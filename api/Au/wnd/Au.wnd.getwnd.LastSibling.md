# Property `Au.wnd.getwnd.LastSibling`

Gets the last sibling window or control in the Z order. If this is the last, returns this, not `default(wnd)`.

```
public wnd LastSibling { get; }
```

##### Property Value

`Au.wnd`

#### Remarks

If this is a top-level window, gets the last top-level window, else gets the last control of the same direct parent. Calls API `GetWindow`(this, `GW_HWNDLAST`). Supports `Au.lastError`.