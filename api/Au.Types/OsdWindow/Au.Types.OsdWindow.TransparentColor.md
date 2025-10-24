# Property `Au.Types.OsdWindow.TransparentColor`

Gets or sets transparent color, default 0xF5F4F5. Pixels of this color will be transparent, unless `Au.Types.OsdWindow.Opacity` is not 0.

```
public ColorInt TransparentColor { get; set; }
```

##### Property Value

`Au.Types.ColorInt`

#### Remarks

This property cannot be changed after creating OSD window. Note: when used for transparent text, text edges are blended with this color, and it can become visible if the color is not chosen carefully.