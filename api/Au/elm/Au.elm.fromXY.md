# Method `Au.elm.fromXY`

## Overload 1

Gets UI element from point.

```
public static elm fromXY(POINT p, EXYFlags flags = 0)
```

##### Parameters

- *p*  (`Au.Types.POINT`):
    Coordinates. Tip: To specify coordinates relative to the right, bottom, work area or a non-primary screen, use `Au.Types.Coord.Normalize`, like in the example.
- *flags*  (`Au.Types.EXYFlags`)

##### Returns

`Au.elm`

Returns `null` if failed. Usually fails if the window is of a higher [UAC](../articles/UAC.html) integrity level process. With some windows can fail occasionally.

#### Examples

Get UI element at 100 200.

```
var e = elm.fromXY((100, 200));
print.it(e);
```

Get UI element at 50 from left and 100 from the bottom edge of the work area.

```
var e = elm.fromXY(Coord.Normalize(50, ^100, workArea: true));
print.it(e);
```

* * *

## Overload 2

Gets UI element from point.

```
public static elm fromXY(int x, int y, EXYFlags flags = 0)
```

##### Parameters

- *x*  (`int`)
- *y*  (`int`)
- *flags*  (`Au.Types.EXYFlags`)

##### Returns

`Au.elm`

Returns `null` if failed. Usually fails if the window is of a higher [UAC](../articles/UAC.html) integrity level process. With some windows can fail occasionally.

#### Examples

Get UI element at 100 200.

```
var e = elm.fromXY((100, 200));
print.it(e);
```

Get UI element at 50 from left and 100 from the bottom edge of the work area.

```
var e = elm.fromXY(Coord.Normalize(50, ^100, workArea: true));
print.it(e);
```