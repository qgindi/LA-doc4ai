# Method `Au.wnd.IsEnabled`

Returns `true` if the window is enabled for mouse and keyboard input. Returns `false` if disabled. Also `false` if failed (probably window closed or 0 handle). Supports `Au.lastError`.

```
public bool IsEnabled(bool ancestorsToo = false)
```

##### Parameters

- *ancestorsToo*  (`bool`):
    Check whether all ancestors of this control are enabled too. If `false` (default), this function simply calls API `IsWindowEnabled`, which usually returns `true` for controls in disabled windows.

##### Returns

`bool`