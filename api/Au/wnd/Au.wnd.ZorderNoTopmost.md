# Method `Au.wnd.ZorderNoTopmost`

Makes this window non-topmost.

```
public bool ZorderNoTopmost(bool afterActiveWindow = false)
```

##### Parameters

- *afterActiveWindow*  (`bool`):
    Also place this window below the active non-topmost window in the Z order, unless the active window is this or owner.

##### Returns

`bool`

#### Remarks

This cannot be a control. Also affects owner and owned windows. Uses API `SetWindowPos`. Supports `Au.lastError`.