# Property `Au.wnd.RectInDirectParent`

Gets child window rectangle in the client area of the direct parent window.

```
public RECT RectInDirectParent { get; }
```

##### Property Value

`Au.Types.RECT`

#### Remarks

Calls `Au.wnd.getwnd.DirectParent` and `Au.wnd.GetRectIn`. Returns `default(RECT)` if fails (eg window closed).