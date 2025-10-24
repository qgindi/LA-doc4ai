# Property `Au.wnd.Screen`

Gets `Au.screen` of the screen that contains this window (the biggest part of it) or is nearest to it. If this window handle is `default(wnd)` or invalid, gets the primary screen. Calls `Au.screen.of`.

```
public screen Screen { get; }
```

##### Property Value

`Au.screen`