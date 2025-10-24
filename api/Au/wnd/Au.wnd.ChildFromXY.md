# Method `Au.wnd.ChildFromXY`

## Overload 1

Gets descendant control from point.

```
public wnd ChildFromXY(Coord x, Coord y, WXYCFlags flags = 0)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X coordinate in client area or screen (if flag `ScreenXY`). Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate.
- *flags*  (`Au.Types.WXYCFlags`)

##### Returns

`Au.wnd`

By default returns `default(wnd)` if the point is not in a child control; it depends on *flags*.

##### Exceptions

- `Au.Types.AuWndException`:
    This variable is invalid (window not found, closed, etc).

* * *

## Overload 2

Gets descendant control from point.

```
public wnd ChildFromXY(POINT p, WXYCFlags flags = 0)
```

##### Parameters

- *p*  (`Au.Types.POINT`):
    Coordinates in client area or screen (if flag `ScreenXY`).
- *flags*  (`Au.Types.WXYCFlags`)

##### Returns

`Au.wnd`

By default returns `default(wnd)` if the point is not in a child control; it depends on *flags*.

##### Exceptions

- `Au.Types.AuWndException`:
    This variable is invalid (window not found, closed, etc).