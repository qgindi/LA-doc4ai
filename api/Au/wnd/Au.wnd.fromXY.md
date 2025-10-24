# Method `Au.wnd.fromXY`

## Overload 1

Gets visible top-level window or control from point.

```
public static wnd fromXY(POINT p, WXYFlags flags = 0)
```

##### Parameters

- *p*  (`Au.Types.POINT`):
    Coordinates. Tip: To specify coordinates relative to the right, bottom, work area or a non-primary screen, use `Au.Types.Coord.Normalize`, like in the example.
- *flags*  (`Au.Types.WXYFlags`)

##### Returns

`Au.wnd`

#### Remarks

Unlike API `WindowFromPhysicalPoint` etc, this function: does not skip disabled controls; always skips transparent control like group box if a smaller sibling is there. All this is not true with flag `Raw`.

#### Examples

Find window at 100 200.

```
var w = wnd.FromXY((100, 200), WXYFlags.NeedWindow);
print.it(w);
```

Find window or control at 50 from left and 100 from bottom of the work area.

```
var w = wnd.FromXY(Coord.Normalize(50, ^100, workArea: true));
print.it(w);
```

* * *

## Overload 2

Gets visible top-level window or control from point.

```
public static wnd fromXY(int x, int y, WXYFlags flags = 0)
```

##### Parameters

- *x*  (`int`)
- *y*  (`int`)
- *flags*  (`Au.Types.WXYFlags`)

##### Returns

`Au.wnd`

#### Remarks

Unlike API `WindowFromPhysicalPoint` etc, this function: does not skip disabled controls; always skips transparent control like group box if a smaller sibling is there. All this is not true with flag `Raw`.

#### Examples

Find window at 100 200.

```
var w = wnd.FromXY((100, 200), WXYFlags.NeedWindow);
print.it(w);
```

Find window or control at 50 from left and 100 from bottom of the work area.

```
var w = wnd.FromXY(Coord.Normalize(50, ^100, workArea: true));
print.it(w);
```