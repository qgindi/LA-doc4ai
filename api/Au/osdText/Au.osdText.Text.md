# Property `Au.osdText.Text`

Text in OSD window.

```
public string Text { get; set; }
```

##### Property Value

`string`

#### Remarks

This property can be changed after creating OSD window; then the window is not moved/resized, unless `Au.osdText.ResizeWhenContentChanged` is `true`.