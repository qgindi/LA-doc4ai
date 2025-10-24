# Property `Au.osdText.Rect`

Gets or sets OSD window size and position in screen.

```
public override RECT Rect { get; set; }
```

##### Property Value

`Au.Types.RECT`

##### Overrides

`Au.Types.OsdWindow.Rect`

#### Remarks

Normally don't need to use this property. If not used, the OSD window size depends on text etc, and position on `Au.osdText.XY`. This property can be changed after creating OSD window.

### See Also

`Au.osdText.Measure`