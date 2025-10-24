# Property `Au.toolbar.AutoSizeWrapWidth`

When `Au.toolbar.AutoSize` is `true`, this is the preferred width at which buttons are moved to the next row. Unlimited if 0.

```
public double AutoSizeWrapWidth { get; set; }
```

##### Property Value

`double`

#### Remarks

The unit of measurement depends on `Au.toolbar.DpiScaling`.

This property is updated when the user resizes the toolbar while `Au.toolbar.AutoSize` is `true`. It is saved.

If layout of this toolbar is vertical, just sets max width.