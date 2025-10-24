# Struct `Au.Types.IFImage`

Image(s) or color(s) for `Au.uiimage.find` and similar functions.

```
public struct IFImage
```

##### Remarks

Has implicit conversions from:

- string - path of `.png` or `.bmp` file. If not full path, uses `Au.folders.ThisAppImages`.
- string that starts with `"resources/"` or has prefix `"resource:"` - resource name; see `Au.More.ResourceUtil.GetGdipBitmap`.
- string with prefix `"image:"` - Base64 encoded `.png` image.
 Can be created with tool **Find image or color in window** or with function `Au.Controls.KImageUtil.ImageToString` (in `Au.Controls.dll`).
- `Au.Types.ColorInt`, `int` or `uint` in `0xRRGGBB` color format, `System.Drawing.Color` - color. Alpha isn't used.
- `System.Drawing.Bitmap` - image object.
- `IFImage[]` - multiple images or/and colors. Action - find any. To create a different action can be used callback function (parameter *also*).

Icons are not supported directly; you can use `Au.icon` to get icon and convert to bitmap.

### Properties

`Value`

### Operators

`implicit operator IFImage(ColorInt)`, `implicit operator IFImage(IFImage[])`, `implicit operator IFImage(Bitmap)`, `implicit operator IFImage(Color)`, `implicit operator IFImage(int)`, `implicit operator IFImage(string)`, `implicit operator IFImage(uint)`, `implicit operator IFImage(Color)`