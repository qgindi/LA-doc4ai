# Method `Au.wpfBuilder.FormatText`

Adds inlines (text, formatted text, hyperlinks, images, etc) to the last added `System.Windows.Controls.TextBlock` etc.

```
public wpfBuilder FormatText(wpfBuilder.InterpolatedString text)
```

##### Parameters

- *text*  (`Au.wpfBuilder`.`Au.wpfBuilder.InterpolatedString`):

    Interpolated string (like `$"string"`) with tags etc. The format is XML without root element.

    These tags add inlines of these types:

    - `<b>text</b>` - `System.Windows.Documents.Bold`.
    - `<i>text</i>` - `System.Windows.Documents.Italic`.
    - `<u>text</u>` - `System.Windows.Documents.Underline`.
    - `<s>text</s>` - `System.Windows.Documents.Span`.
    - `<s {Span}>text</s>` - `System.Windows.Documents.Span` or a `System.Windows.Documents.Span`-based type. The function adds `text` to its `Inlines` collection.
    - `<a {Action or Action<Hyperlink>}>text</a>` - `System.Windows.Documents.Hyperlink` that calls the action.
    - `<a href='URL or path etc'>text</a>` - `System.Windows.Documents.Hyperlink` that calls `Au.run.itSafe`.

    Tags can have these attributes, like `<s c='red' FontSize = '20'>text</s>`:

    - `c` or `Foreground` - text color, like `'red'` or `'#AARRGGBB'` or `'#RRGGBB'` or `'#ARGB'` or `'#RGB'`.
    - `b` or `Background` - background color.
    - `FontFamily` - font name, like `'Consolas'`.
    - `FontSize` - font size, like `'20'`.
    - `ToolTip` - tooltip text.

    WPF elements of these types can be inserted without tags:

    - `{Inline}` - any inline, eg `System.Windows.Documents.Run`. See also `<s {Span}>text</s>`.
    - `{UIElement}` - a WPF element, eg `System.Windows.Controls.CheckBox` or `System.Windows.Controls.Image`.
    - `{ImageSource}` - adds `System.Windows.Controls.Image`.
    - `{IEnumerable<Inline>}` - adds multiple `System.Windows.Documents.Inline`.

    XML special characters must be escaped:

    - `<` - `&lt;`.
    - `&` - `&amp;`.
    - `'`, `"` - `&apos;` in `'attribute'` or `&quot;` in `"attribute"`.

    The `text` in above examples can contain nested tags and elements. The `<a>` tag creates an image hyperlink if `text` is `{image}`, where image is a `System.Windows.UIElement` with image (see `Au.More.ImageUtil.LoadWpfImageElement`) or `System.Windows.Media.ImageSource` (see `Au.More.ImageUtil.LoadWpfImage`, `Au.icon.ToWpfImage`).

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    Unsupported type of the last added element. Or supported type but non-empty `Content` and `Header` (read Remarks).
- `ArgumentException`:
    Unknown `<tag>` or unsupported `{object}` type.
- `InvalidOperationException`:
    The same `{Span}` or `{Inline}` object in multiple places.
- `FormatException`:
    Invalid color attribute.
- `Exception`:
    Exceptions of `System.Xml.Linq.XElement.Parse`.

#### Remarks

The last added element can be of type:

- `System.Windows.Controls.TextBlock` - the function adds inlines to its `Inlines` collection.
- `System.Windows.Controls.ContentControl` (eg `System.Windows.Controls.Label` or `System.Windows.Controls.Button`) - creates new `System.Windows.Controls.TextBlock` with inlines and sets its `Content` property if it is `null`. If `System.Windows.Controls.HeaderedContentControl` (eg `System.Windows.Controls.GroupBox`) and its `Header` property is `null`, sets `Header` instead.
- `Au.wpfBuilder.Panel` whose `Parent` is `System.Windows.Controls.HeaderedContentControl` (eg `b.StartGrid<GroupBox>(null).FormatText($"...")`) - uses the `System.Windows.Controls.HeaderedContentControl` like the above.

For elements other than the last added use `Au.wpfBuilder.formatTextOf` or `Au.wpfBuilder.formattedText`.

To load images can be used `Au.More.ImageUtil.LoadWpfImageElement` and `Au.More.ImageUtil.LoadWpfImage`.

#### Examples

```
b.R.Add<TextBlock>().FormatText($"""
Text <b>bold</b> <i>italic <u>underline</u>.</i>
<s c='GreenYellow' b='Black' FontFamily='Consolas' FontSize='20'>attributes</s>
<s {new Span() { Foreground = Brushes.Red, Background = new LinearGradientBrush(Colors.GreenYellow, Colors.Transparent, 90) }}>Span object, <b>bold</b></s>
<a href='https://www.example.com'>example.com</a> <b><a href='notepad.exe'>Notepad</a></b>
<a {() => { print.it("click"); }}>click</a> <a {(Hyperlink h) => { print.it("click once"); h.IsEnabled = false; }}>click once</a>
<a {() => { print.it("click"); }} ToolTip='image hyperlink'>{ImageUtil.LoadWpfImageElement("*Entypo.HelpWithCircle #008EEE @14")}</a>
{new Run("Run object") { Foreground = Brushes.Blue, Background = Brushes.Goldenrod, FontSize = 20 }}
Image {ImageUtil.LoadWpfImageElement("*PixelartIcons.Notes #0060F0")}<!-- or ImageUtil.LoadWpfImage(@"C:\Test\image.png") -->
Controls {new TextBox() { MinWidth = 100, Height = 20, Margin = new(3) }} {new CheckBox() { Content = "Check" }}
""");
```

Build interpolated string at run time.

```
wpfBuilder.InterpolatedString s = new();
s.AppendLiteral("Text <b>bold</b> <a ");
s.AppendFormatted(() => { print.it("click"); });
s.AppendLiteral(">link</a>.");
b.R.Add<TextBlock>().FormatText(s);
```