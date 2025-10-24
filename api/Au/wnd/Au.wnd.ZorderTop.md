# Method `Au.wnd.ZorderTop`

Places this window or control at the top of the Z order. Does not activate. If the window was topmost, it will be at the top of topmost windows, else at the top of other windows.

```
public bool ZorderTop(bool ownerToo = false)
```

##### Parameters

- *ownerToo*  (`bool`):
    Place owner windows below this window. If `false` (default), does it only if they otherwise would be on top of this window.

##### Returns

`bool`

#### Remarks

Also affects owner and owned windows. Uses API `SetWindowPos`. Supports `Au.lastError`.