# Method `Au.Types.Coord.NormalizeInWindow`

Returns normal coordinates relative to the client area of a window. Converts fractional/reverse coordinates etc.

```
public static POINT NormalizeInWindow(Coord x, Coord y, wnd w, bool nonClient = false, bool centerIfEmpty = false)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X coordinate relative to the client area of *w*.
- *y*  (`Au.Types.Coord`):
    Y coordinate relative to the client area of *w*.
- *w*  (`Au.wnd`):
    The window.
- *nonClient*  (`bool`):
    *x* *y* are relative to the entire *w* rectangle, not to its client area.
- *centerIfEmpty*  (`bool`):
    If *x* or *y* is `default`, use `Au.Types.Coord.Center`.

##### Returns

`Au.Types.POINT`