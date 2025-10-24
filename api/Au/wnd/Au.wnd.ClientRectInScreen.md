# Property `Au.wnd.ClientRectInScreen`

Gets client area rectangle (width and height) in screen.

```
public RECT ClientRectInScreen { get; }
```

##### Property Value

`Au.Types.RECT`

#### Remarks

Calls `Au.wnd.GetClientRect`. Returns `default(RECT)` if fails (eg window closed).