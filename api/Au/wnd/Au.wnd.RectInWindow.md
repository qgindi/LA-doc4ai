# Property `Au.wnd.RectInWindow`

Gets child window rectangle in the client area of the top-level parent window.

```
public RECT RectInWindow { get; }
```

##### Property Value

`Au.Types.RECT`

#### Remarks

Calls `Au.wnd.Window` and `Au.wnd.GetRectIn`. Returns `default(RECT)` if fails (eg window closed).