# Method `Au.More.CaptureScreen.Pixels`

## Overload 1

Gets pixel colors from a rectangle in screen.

```
public static uint[,] Pixels(RECT r)
```

##### Parameters

- *r*  (`Au.Types.RECT`):
    Rectangle in screen.

##### Returns

`uint`[,]

2-dimensional array `[row, column]` containing pixel colors in `0xAARRGGBB` format. Alpha `0xFF`.

##### Exceptions

- `ArgumentException`:
    Empty rectangle.
- `Au.Types.AuException`:
    Failed. Probably there is not enough memory for bitmap of this size (`width*height*4` bytes).

#### Examples

```
print.clear();
var a = CaptureScreen.Pixels(new(100, 100, 4, 10));
for(int i = 0, nRows = a.GetLength(0); i < nRows; i++) print.it(a[i,0], a[i,1], a[i,2], a[i,3]);
```

* * *

## Overload 2

Gets pixel colors from a rectangle in window client area.

```
public static uint[,] Pixels(wnd w, RECT? r = null, CIFlags flags = CIFlags.WindowDC)
```

##### Parameters

- *w*  (`Au.wnd`):
    Window or control.
- *r*  (`Au.Types.RECT?`):
    Rectangle in *w* client area coordinates. If `null`, uses `w.ClientRect`.
- *flags*  (`Au.Types.CIFlags`)

##### Returns

`uint`[,]

2-dimensional array `[row, column]` containing pixel colors in `0xAARRGGBB` format. Alpha `0xFF`.

##### Exceptions

- `Au.Types.AuWndException`:
    Invalid *w*.
- `ArgumentException`:
    The rectangle is empty or does not intersect with the window's client area.
- `Au.Types.AuException`:
    Failed. For example there is not enough memory for bitmap of this size (`width*height*4` bytes).

#### Remarks

If *flags* contains `WindowDC` (default) or `PrintWindow`:

- If the window is partially or completely transparent, captures its non-transparent view.
- If the window is DPI-scaled, captures its non-scaled view. However *r* must contain scaled coordinates.