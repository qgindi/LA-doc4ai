# Property `Au.screen.ofActiveWindow`

Returns a lazy `Au.screen` variable that later will get the screen of the active window at that time.

```
public static screen ofActiveWindow { get; }
```

##### Property Value

`Au.screen`

#### Remarks

If need non-lazy: `screen.of(wnd.active)` or `screen.ofActiveWindow.Now`.