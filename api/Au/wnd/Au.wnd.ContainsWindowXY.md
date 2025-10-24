# Method `Au.wnd.ContainsWindowXY`

## Overload 1

Returns `true` if this control (its rectangle) contains the specified point in parent window.

```
public bool ContainsWindowXY(wnd parent, Coord x, Coord y)
```

##### Parameters

- *parent*  (`Au.wnd`):
    Direct or indirect parent window. The coordinates are relative to its client area. Actually this and parent can be any windows or controls, the function does not check whether this is a child of parent.
- *x*  (`Au.Types.Coord`):
    X coordinate. Not used if `default`. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate. Not used if `default`.

##### Returns

`bool`

* * *

## Overload 2

This overload calls `Au.wnd.ContainsWindowXY(wnd, Coord, Coord)` with `Au.wnd.Window`, *x* and *y*.

```
public bool ContainsWindowXY(Coord x, Coord y)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X coordinate. Not used if `default`. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate. Not used if `default`.

##### Returns

`bool`