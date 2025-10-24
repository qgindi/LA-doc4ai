# Method `Au.wnd.MoveInScreen`

Moves this window to coordinates *x y* in specified screen, and ensures that entire window is in that screen.

```
public void MoveInScreen(Coord x, Coord y, screen screen = default, bool workArea = true, bool ensureInScreen = true)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X coordinate in the specified screen. If `default` - screen center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate in the specified screen. If `default` - screen center.
- *screen*  (`Au.screen`):
    Move to this screen (see `Au.screen`). If default, uses screen of this window. Example: `screen.index(1)`.
- *workArea*  (`bool`):
    Use the work area, not whole screen. Default `true`.
- *ensureInScreen*  (`bool`):
    If part of window is not in screen, move and/or resize it so that entire window would be in screen. Default `true`.

##### Exceptions

- `Au.Types.AuWndException`

#### Remarks

If the window is maximized, minimized or hidden, it will have the new position and size when restored, not immediately, except when moving maximized to another screen.

### See Also

`Au.Types.RECT.MoveInScreen`