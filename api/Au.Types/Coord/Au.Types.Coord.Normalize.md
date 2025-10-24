# Method `Au.Types.Coord.Normalize`

Returns normal coordinates relative to the primary screen. Converts fractional/reverse coordinates etc.

```
public static POINT Normalize(Coord x, Coord y, bool workArea = false, screen screen = default, bool widthHeight = false, bool centerIfEmpty = false)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X coordinate relative to the specified screen (`default` - primary).
- *y*  (`Au.Types.Coord`):
    Y coordinate relative to the specified screen (`default` - primary).
- *workArea*  (`bool`):
    *x* *y* are relative to the work area.
- *screen*  (`Au.screen`):
    If used, *x* *y* are relative to this screen. Default - primary screen. Example: `screen.index(1)`.
- *widthHeight*  (`bool`):
    Use only width and height of the screen rectangle. If `false`, the function adds its offset (left and top, which can be nonzero if using the work area or a non-primary screen).
- *centerIfEmpty*  (`bool`):
    If *x* or *y* is `default`, use `Au.Types.Coord.Center`.

##### Returns

`Au.Types.POINT`