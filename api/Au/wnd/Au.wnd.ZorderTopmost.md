# Method `Au.wnd.ZorderTopmost`

Makes this window topmost (always on top of non-topmost windows in the Z order). Does not activate.

```
public bool ZorderTopmost()
```

##### Returns

`bool`

#### Remarks

This cannot be a control. Also affects owned windows. Does not affect owners. Uses API `SetWindowPos`. Supports `Au.lastError`.