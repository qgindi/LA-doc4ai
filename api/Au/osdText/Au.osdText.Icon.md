# Property `Au.osdText.Icon`

Icon or image at the left. Any size.

```
public object Icon { get; set; }
```

##### Property Value

`object`

`Au.icon`, `System.Drawing.Icon` or `System.Drawing.Image`.

#### Remarks

For example `System.Drawing.SystemIcons.Information` or `icon.stock(StockIcon.INFO)` or `ImageUtil.LoadGdipBitmapFromXaml("XAML copied from the Icons tool. You can edit, Width, Height and Fill (color).", screen.primary.Dpi)`.

This property cannot be changed after creating OSD window.