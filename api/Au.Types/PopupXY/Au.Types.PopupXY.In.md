# Method `Au.Types.PopupXY.In`

Creates new `Au.Types.PopupXY` that specifies position in a rectangle. For example of the owner window.

```
public static PopupXY In(RECT r, Coord x = default, Coord y = default)
```

##### Parameters

- *r*  (`Au.Types.RECT`):
    Rectangle relative to the primary screen.
- *x*  (`Au.Types.Coord`):
    X relative to the rectangle. Default - center.
- *y*  (`Au.Types.Coord`):
    Y relative to the rectangle. Default - center.

##### Returns

`Au.Types.PopupXY`