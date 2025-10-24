# Property `Au.wpfBuilder.winWhite`

If `true`, `wpfBuilder` constructors used afterwards will not change the window background color.

```
public static bool winWhite { get; set; }
```

##### Property Value

`bool`

#### Remarks

If `true`, `wpfBuilder` constructors don't change the background color; then the color depends on theme. If `false` constructors set standard color of dialog windows, usually light gray. Default value depends on application's theme and usually is `true` if using a custom theme.