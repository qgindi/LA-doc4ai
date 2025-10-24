# Property `Au.wnd.getwnd.DirectParent`

Gets the direct parent window of this control. It can be the top-level window or another control.

```
public wnd DirectParent { get; }
```

##### Property Value

`Au.wnd`

`default(wnd)` if this is a top-level window or if failed.

#### Remarks

Supports `Au.lastError`. Unlike API `GetParent`, this function never returns the owner window.