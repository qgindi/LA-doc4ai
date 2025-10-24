# Property `Au.osdText.IsOfImageSize`

When used `Au.osdText.BackgroundImage`, the OSD window has the same size as the image, plus borders. Else OSD window size is calculated from sizes of text and icon. Then image is displayed scaled or clipped if need.

```
public bool IsOfImageSize { get; set; }
```

##### Property Value

`bool`

#### Remarks

This property cannot be changed after creating OSD window.