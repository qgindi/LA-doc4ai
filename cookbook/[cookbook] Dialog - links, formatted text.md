# Dialog - links, formatted text

To display static text with formatting, links and images, can be used WPF elements of type `TextBlock`. Function `Au.wpfBuilder.FormatText` makes it easier.

```
using System.Windows;
using System.Windows.Controls;
using System.Windows.Documents;
using System.Windows.Media;

var b = new wpfBuilder("Window").WinSize(400);
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
&lt; &gt; &amp; &apos; &quot;
""");
b.R.AddOkCancel();
b.End();
if (!b.ShowDialog()) return;
```