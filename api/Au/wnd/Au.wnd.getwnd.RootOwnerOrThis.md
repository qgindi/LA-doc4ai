# Method `Au.wnd.getwnd.RootOwnerOrThis`

Gets the bottom-most owner window in the chain of owner windows of this window. If this window is not owned, returns this window.

```
public wnd RootOwnerOrThis(bool supportControls = false)
```

##### Parameters

- *supportControls*  (`bool`):
    If this is a child window, use its top-level parent window instead.

##### Returns

`Au.wnd`

`default(wnd)` if failed.

#### Remarks

Supports `Au.lastError`.