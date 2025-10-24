# Method `Au.Types.RECT.MoveInScreen`

Moves this rectangle to the specified coordinates in the specified screen, and ensures that whole rectangle is in screen. Final rectangle coordinates are relative to the primary screen.

```
public void MoveInScreen(Coord x, Coord y, screen screen = default, bool workArea = true, bool ensureInScreen = true)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X coordinate in the specified screen. If `default` - center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate in the specified screen. If `default` - center.
- *screen*  (`Au.screen`):
    Use this screen. If `default`, uses the primary screen. Example: `screen.index(1)`.
- *workArea*  (`bool`):
    Use the work area, not whole screen. Default `true`.
- *ensureInScreen*  (`bool`):
    If part of rectangle is not in screen, move and/or resize it so that entire rectangle would be in screen. Default `true`.

#### Remarks

This function can be used to calculate new window location before creating it. If window already exists, use `Au.wnd.MoveInScreen`.