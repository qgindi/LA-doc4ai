# Method `Au.wnd.SetWindowLong`

Calls API `SetWindowLongPtr`.

```
public nint SetWindowLong(int index, nint newValue, bool noException = false)
```

##### Parameters

- *index*  (`int`):
    A constant from `Au.Types.GWL`, or an offset in window memory reserved when registering window class.
- *newValue*  (`nint`):
    New value.
- *noException*  (`bool`):
    Don't throw exception when fails.

##### Returns

`nint`

Previous value. If fails and *noException* `true`, returns 0, and can be used `Au.lastError`.

##### Exceptions

- `Au.Types.AuWndException`

#### Remarks

See also API `SetWindowSubclass`.