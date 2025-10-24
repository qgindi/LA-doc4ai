# Property `Au.wnd.getwnd.Owner`

Gets the owner window of this top-level window.

```
public wnd Owner { get; }
```

##### Property Value

`Au.wnd`

`default(wnd)` if this window isn't owned or if failed.

#### Remarks

A window that has an owner window is always on top of it. Controls don't have an owner window. Supports `Au.lastError`.

### See Also

`Au.More.WndUtil.SetOwnerWindow`