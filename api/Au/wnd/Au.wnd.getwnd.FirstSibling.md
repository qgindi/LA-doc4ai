# Property `Au.wnd.getwnd.FirstSibling`

Gets the first sibling window or control in the Z order. If this is the first, returns this.

```
public wnd FirstSibling { get; }
```

##### Property Value

`Au.wnd`

#### Remarks

If this is a top-level window, gets the first top-level window, else gets the first control of the same direct parent. Calls API `GetWindow`(this, `GW_HWNDFIRST`). Supports `Au.lastError`.