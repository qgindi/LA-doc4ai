# Property `Au.toolbar.DpiScaling`

Whether to DPI-scale toolbar size and offsets. Default: scale size; scale offsets if anchor is not screen.

```
public TBScaling DpiScaling { get; set; }
```

##### Property Value

`Au.Types.TBScaling`

#### Remarks

The unit of measurement of `Au.toolbar.Size`, `Au.toolbar.Offsets` and some other properties depends on whether scaling is used for that property. If scaling is used, the unit is logical pixels; it is 1/96 inch regardless of screen DPI. If scaling not used, the unit is physical pixels. Screen DPI can be changed in Windows Settings; when it is 100%, logical and physical pixels are equal.