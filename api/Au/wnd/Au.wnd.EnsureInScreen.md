# Method `Au.wnd.EnsureInScreen`

Moves this window if need, to ensure that entire window is in that screen.

```
public void EnsureInScreen(screen screen = default, bool workArea = true)
```

##### Parameters

- *screen*  (`Au.screen`):
    Move to this screen (see `Au.screen`). If default, uses screen of this window.
- *workArea*  (`bool`):
    Use the work area, not whole screen. Default `true`.

##### Exceptions

- `Au.Types.AuWndException`

#### Remarks

If the window is maximized, minimized or hidden, it will have the new position and size when restored, not immediately.

### See Also

`Au.Types.RECT.EnsureInScreen`