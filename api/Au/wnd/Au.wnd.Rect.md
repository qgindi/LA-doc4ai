# Property `Au.wnd.Rect`

Gets rectangle (position and size) in screen coordinates.

```
public RECT Rect { get; }
```

##### Property Value

`Au.Types.RECT`

#### Remarks

Calls `Au.wnd.GetRect`. Returns `default(RECT)` if fails (eg window closed). Supports `Au.lastError`.