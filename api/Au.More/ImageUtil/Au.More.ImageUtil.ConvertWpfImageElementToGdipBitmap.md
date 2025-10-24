# Method `Au.More.ImageUtil.ConvertWpfImageElementToGdipBitmap`

Converts WPF image element to GDI+ image.

```
public static Bitmap ConvertWpfImageElementToGdipBitmap(FrameworkElement e, int dpi, SIZE? size = null)
```

##### Parameters

- *e*  (`FrameworkElement`):
    For example `System.Windows.Controls.Viewbox`.
- *dpi*  (`int`):
    DPI of window that will display the image.
- *size*  (`Au.Types.SIZE?`):
    Final image size in logical pixels (not DPI-scaled). If `null`, uses element's `DesiredSize` property, max 1024x1024. If not `null`, sets element's `Width` and `Height`; the element should not be used in UI.

##### Returns

`Bitmap`

New `Bitmap`. Note: its pixel format is `Format32bppPArgb` (premultiplied ARGB).