# Constructor of `Au.Types.PopupXY`

Sets position and/or screen.

```
public PopupXY(Coord x = default, Coord y = default, bool workArea = true, screen screen = default)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X relative to the screen or work area. Default - center.
- *y*  (`Au.Types.Coord`):
    X relative to the screen or work area. Default - center.
- *workArea*  (`bool`):
    *x y* are relative to the work area of the screen.
- *screen*  (`Au.screen`):
    Can be used to specify a screen. Default - primary. Example: `screen.index(1)`.

#### Remarks

Also there is are implicit conversions from tuple (x, y) and `Au.Types.POINT`. Instead of `new PopupXY(x, y)` you can use `(x, y)`. Instead of `new PopupXY(p.x, p.y, false)` you can use `p` or `(POINT)p` .