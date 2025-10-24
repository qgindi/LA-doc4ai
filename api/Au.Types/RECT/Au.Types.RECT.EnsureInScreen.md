# Method `Au.Types.RECT.EnsureInScreen`

Adjusts this rectangle to ensure that whole rectangle is in screen. Initial and final rectangle coordinates are relative to the primary screen.

```
public void EnsureInScreen(screen screen = default, bool workArea = true)
```

##### Parameters

- *screen*  (`Au.screen`):
    Use this screen (see `Au.screen`). If `default`, uses screen of the rectangle (or nearest).
- *workArea*  (`bool`):
    Use the work area, not whole screen. Default `true`.

#### Remarks

This function can be used to calculate new window location before creating it. If window already exists, use `Au.wnd.EnsureInScreen`.