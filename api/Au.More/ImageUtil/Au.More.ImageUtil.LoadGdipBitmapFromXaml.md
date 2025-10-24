# Method `Au.More.ImageUtil.LoadGdipBitmapFromXaml`

Loads GDI+ image from WPF XAML file or string.

```
public static Bitmap LoadGdipBitmapFromXaml(string image, int dpi, SIZE? size = null)
```

##### Parameters

- *image*  (`string`):
    XAML file, resource or string. See `Au.More.ImageUtil.LoadWpfImageElement`.
- *dpi*  (`int`):
    DPI of window that will display the image.
- *size*  (`Au.Types.SIZE?`):
    Final image size in logical pixels (not DPI-scaled). If `null`, uses element's `DesiredSize` property, max 1024x1024.

##### Returns

`Bitmap`

New `Bitmap`. Note: its pixel format is `Format32bppPArgb` (premultiplied ARGB).

##### Exceptions

- `Exception`

#### Remarks

Calls `Au.More.ImageUtil.LoadWpfImageElement` and `Au.More.ImageUtil.ConvertWpfImageElementToGdipBitmap`. Don't use the `Tag` property of the bitmap. It keeps bitmap data.