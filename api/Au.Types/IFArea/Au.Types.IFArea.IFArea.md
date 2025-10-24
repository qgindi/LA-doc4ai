# Constructor of `Au.Types.IFArea`

## Overload 1

Specifies a window or control and a rectangle in its client area.

```
public IFArea(wnd w, RECT r)
```

##### Parameters

- *w*  (`Au.wnd`)
- *r*  (`Au.Types.RECT`)

* * *

## Overload 2

Specifies a UI element and a rectangle in it.

```
public IFArea(elm e, RECT r)
```

##### Parameters

- *e*  (`Au.elm`)
- *r*  (`Au.Types.RECT`)

* * *

## Overload 3

Specifies a window or control and a rectangle in its client area. The parameters are of `Au.Types.Coord` type, therefore can be easily specified reverse and fractional coordinates, like `^10` and `.5f`. Use `^0` for right or bottom edge.

```
public IFArea(wnd w, Coord left, Coord top, Coord right, Coord bottom)
```

##### Parameters

- *w*  (`Au.wnd`)
- *left*  (`Au.Types.Coord`)
- *top*  (`Au.Types.Coord`)
- *right*  (`Au.Types.Coord`)
- *bottom*  (`Au.Types.Coord`)

* * *

## Overload 4

Specifies a UI element and a rectangle in it. The parameters are of `Au.Types.Coord` type, therefore can be easily specified reverse and fractional coordinates, like `^10` and `.5f`. Use `^0` for right or bottom edge.

```
public IFArea(elm e, Coord left, Coord top, Coord right, Coord bottom)
```

##### Parameters

- *e*  (`Au.elm`)
- *left*  (`Au.Types.Coord`)
- *top*  (`Au.Types.Coord`)
- *right*  (`Au.Types.Coord`)
- *bottom*  (`Au.Types.Coord`)