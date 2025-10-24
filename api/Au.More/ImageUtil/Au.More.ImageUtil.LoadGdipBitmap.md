# Method `Au.More.ImageUtil.LoadGdipBitmap`

Loads GDI+ image from file, resource or string.

```
public static Bitmap LoadGdipBitmap(string image, (int dpi, SIZE? size)? xaml = null)
```

##### Parameters

- *image*  (`string`):

    Can be:

    - file path. Can have prefix `"imagefile:"`.
    - resource path that starts with `"resources/"` or has prefix `"resource:"` (`Au.More.ResourceUtil.GetGdipBitmap`)
    - Base64 encoded image string with prefix `"image:"`.
- *xaml*  (`(int dpi, SIZE? size)?`):
    If not `null`, supports XAML images. See `Au.More.ImageUtil.LoadGdipBitmapFromXaml`.

##### Returns

`Bitmap`

##### Exceptions

- `Exception`:
    Depending on *image* string format, exceptions of `System.IO.File.OpenRead`, `System.Drawing.Bitmap.Bitmap`, etc.