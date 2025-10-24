# Operator `Au.Types.PopupXY.implicit operator`

## Overload 1

Creates new `Au.Types.PopupXY` that specifies position relative to the work area of the primary screen.

```
public static implicit operator PopupXY((Coord x, Coord y) p)
```

##### Parameters

- *p*  (`(Coord x, Coord y)`)

##### Returns

`Au.Types.PopupXY`

* * *

## Overload 2

Creates new `Au.Types.PopupXY` that specifies position relative to the primary screen (not to the work area).

```
public static implicit operator PopupXY(POINT p)
```

##### Parameters

- *p*  (`Au.Types.POINT`)

##### Returns

`Au.Types.PopupXY`