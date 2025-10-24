# Method `Au.wnd.Move`

## Overload 1

Moves and/or resizes.

```
public void Move(Coord x, Coord y, Coord width, Coord height, bool workArea = false, screen screen = default, bool visibleRect = false)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    Left. If `default`, does not move in X axis. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Top. If `default`, does not move in Y axis.
- *width*  (`Au.Types.Coord`):
    Width. If `default`, does not change width.
- *height*  (`Au.Types.Coord`):
    Height. If `default`, does not change height.
- *workArea*  (`bool`):
    *x y width height* are relative to the work area. This parameter not used with child windows.
- *screen*  (`Au.screen`):
    *x y width height* are relative to this screen or its work area. Default - primary. Example: `screen.index(1)`. This parameter not used with child windows.
- *visibleRect*  (`bool`):
    Use the visible rectangle without the transparent frame. Note: the window should be visible. This parameter not used with child windows.

##### Exceptions

- `Au.Types.AuWndException`

#### Remarks

Also restores the visible top-level window if it is minimized or maximized. For top-level windows use screen coordinates. For controls - direct parent client area coordinates. With windows of current thread usually it's better to use `Au.wnd.MoveL`.

* * *

## Overload 2

Moves.

```
public void Move(Coord x, Coord y, bool workArea = false, screen screen = default, bool visibleRect = false)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    Left. If `default`, does not move in X axis. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Top. If `default`, does not move in Y axis.
- *workArea*  (`bool`):
    *x y* are relative to the work area. This parameter not used with child windows.
- *screen*  (`Au.screen`):
    *x y* are relative to this screen or its work area. Default - primary. Example: `screen.index(1)`. This parameter not used with child windows.
- *visibleRect*  (`bool`):
    Use the visible rectangle without the transparent frame. Note: the window should be visible. This parameter not used with child windows.

##### Exceptions

- `Au.Types.AuWndException`

#### Remarks

Also restores the visible top-level window if it is minimized or maximized. For top-level windows use screen coordinates. For controls - direct parent client area coordinates. With windows of current thread usually it's better to use `Au.wnd.MoveL`.