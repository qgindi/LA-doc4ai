# Class `Au.clipboardData`

Sets or gets clipboard data in multiple formats.

```
public class clipboardData
```

##### Remarks

The `AddX` functions add data to the variable (not to the clipboard). Then `Au.clipboardData.SetClipboard` copies the added data to the clipboard. Also you can use the variable with `Au.clipboard.pasteData`. The static `GetX` functions get data directly from the clipboard.

##### Examples

Get bitmap image from clipboard.

```
var image = clipboardData.getImage();
if(image == null) print.it("no image in clipboard"); else print.it(image.Size);
```

Set clipboard data in two formats: text and image.

```
new clipboardData().AddText("text").AddImage(Image.FromFile(@"C:\file.png")).SetClipboard();
```

Paste data of two formats: HTML and text.

```
clipboard.pasteData(new clipboardData().AddHtml("<b>text</b>").AddText("text"));
```

Copy data in two formats: HTML and text.

```
string html = null, text = null;
clipboard.copyData(() => { html = clipboardData.getHtml(); text = clipboardData.getText(); });
print.it(html); print.it(text);
```

##### Inheritance

`object` → `clipboardData`

### Methods

`AddBinary`, `AddFiles`, `AddHtml`, `AddImage`, `AddText`, `SetClipboard`, `SetOpenClipboard`, `contains`, `contains`, `getBinary`, `getBinary<T>`, `getFiles`, `getHtml`, `getHtml`, `getImage`, `getText`