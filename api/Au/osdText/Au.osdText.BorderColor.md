# Property `Au.osdText.BorderColor`

Border color. Default: `Au.osdText.defaultBorderColor`.

```
public ColorInt BorderColor { get; set; }
```

##### Property Value

`Au.Types.ColorInt`

#### Remarks

This property can be changed after creating OSD window. No border if `Au.Types.OsdWindow.Opacity`==0 or `BorderColor`==`Au.osdText.BackColor`.