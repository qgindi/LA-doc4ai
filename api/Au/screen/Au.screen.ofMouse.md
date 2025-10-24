# Property `Au.screen.ofMouse`

Returns a lazy `Au.screen` variable that later will get the screen from the mouse cursor position at that time.

```
public static screen ofMouse { get; }
```

##### Property Value

`Au.screen`

#### Remarks

If need non-lazy: `screen.of(mouse.xy)` or `screen.ofMouse.Now`.