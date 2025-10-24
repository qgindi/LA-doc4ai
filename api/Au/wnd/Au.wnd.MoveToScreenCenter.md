# Method `Au.wnd.MoveToScreenCenter`

Moves this window to the center of the screen. Ensures that entire window is in that screen.

```
public void MoveToScreenCenter(screen screen = default)
```

##### Parameters

- *screen*  (`Au.screen`):
    Move to this screen (see `Au.screen`). If default, uses screen of this window.

##### Exceptions

- `Au.Types.AuWndException`

#### Remarks

Calls `ShowNotMinMax(true)` and `MoveInScreen(default, default, screen, true)`. See `Au.wnd.MoveInScreen`.

### See Also

`Au.Types.RECT.MoveInScreen`