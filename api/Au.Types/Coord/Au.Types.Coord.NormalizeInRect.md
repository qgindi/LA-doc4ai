# Method `Au.Types.Coord.NormalizeInRect`

Converts fractional/reverse coordinates to normal coordinates in a rectangle.

```
public static POINT NormalizeInRect(Coord x, Coord y, RECT r, bool widthHeight = false, bool centerIfEmpty = false)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X coordinate relative to *r*.
- *y*  (`Au.Types.Coord`):
    Y coordinate relative to *r*.
- *r*  (`Au.Types.RECT`):
    The rectangle.
- *widthHeight*  (`bool`):
    Use only width and height of *r*. If `false` (default), the function adds *r* offset (left and top).
- *centerIfEmpty*  (`bool`):
    If *x* or *y* is `default`, use `Au.Types.Coord.Center`. Not used with *widthHeight*.

##### Returns

`Au.Types.POINT`