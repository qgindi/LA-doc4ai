# Method `Au.wnd.ActivateL`

Lightweight version of `Au.wnd.Activate`. Does not throw exceptions.

```
public bool ActivateL(bool full = false)
```

##### Parameters

- *full*  (`bool`):
    Call `Au.wnd.Activate` and handle exceptions; on exception return `false`. If `false` (default), just activates; does not show hidden, does not restore minimized, does not check whether it is a top-level window or control, does not check whether activated exactly this window, etc.

##### Returns

`bool`

`false` if failed.