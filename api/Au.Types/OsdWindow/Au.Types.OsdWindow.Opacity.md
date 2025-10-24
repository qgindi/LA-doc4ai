# Property `Au.Types.OsdWindow.Opacity`

Gets or sets the opacity of the OSD window, from 0 to 1. If 1, completely opaque. If 0, pixels of `Au.Types.OsdWindow.TransparentColor` are transparent, others opaque. If between 0 and 1, partially transparent.

```
public double Opacity { get; set; }
```

##### Property Value

`double`

Default is 1. Default in `Au.osdRect` is 0.

#### Remarks

This property can be changed after creating OSD window.