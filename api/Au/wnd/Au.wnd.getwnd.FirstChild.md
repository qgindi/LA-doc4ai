# Property `Au.wnd.getwnd.FirstChild`

Gets the first direct child control in the Z order.

```
public wnd FirstChild { get; }
```

##### Property Value

`Au.wnd`

`default(wnd)` if no children or if failed.

#### Remarks

Calls API `GetWindow`(`GW_CHILD`). Supports `Au.lastError`.