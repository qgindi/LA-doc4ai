# Method `Au.wnd.ZorderAbove`

Places this window above window *w* in the Z order.

```
public bool ZorderAbove(wnd w, bool ownerToo = false)
```

##### Parameters

- *w*  (`Au.wnd`):
    Another window.
- *ownerToo*  (`bool`):
    Place owner windows below this window. If `false` (default), does it only if they otherwise would be on top of this window.

##### Returns

`bool`

#### Remarks

This window and *w* can be both top-level windows or both controls of same parent. Can make this window topmost or non-topmost, depending on where *w* is in the Z order. Also affects owned and owner windows, but does not make them topmost/non-topmost if not necessary. Uses API `SetWindowPos`. Supports `Au.lastError`.