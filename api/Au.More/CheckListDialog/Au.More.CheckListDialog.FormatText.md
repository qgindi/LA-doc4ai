# Method `Au.More.CheckListDialog.FormatText`

Sets formatted text, like `Au.wpfBuilder.FormatText`.

```
public void FormatText(wpfBuilder.InterpolatedString text)
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

##### Exceptions

- `NotSupportedException`:
    Unsupported *obj* type or non-empty `Content`/`Header`.
- `ArgumentException`:
    Unknown `<tag>` or unsupported `{object}` type.
- `InvalidOperationException`:
    The same `{Span}` or `{Inline}` object in multiple places.
- `FormatException`:
    Invalid color attribute.
- `Exception`:
    Exceptions of `System.Xml.Linq.XElement.Parse`.