# Method `Au.More.CaptureScreen.Pixel`

## Overload 1

Gets color of a screen pixel.

```
public static uint Pixel(POINT p)
```

##### Parameters

- *p*  (`Au.Types.POINT`):
    x y in screen.

##### Returns

`uint`

Pixel color in `0xAARRGGBB` format. Alpha 0xFF. Returns 0 if fails, eg if x y is not in screen.

* * *

## Overload 2

Gets color of a window pixel.

```
public static uint Pixel(wnd w, POINT p, CIFlags flags = CIFlags.WindowDC)
```

##### Parameters

- *w*  (`Au.wnd`):
    Window or control.
- *p*  (`Au.Types.POINT`):
    x y in *w* client area.
- *flags*  (`Au.Types.CIFlags`)

##### Returns

`uint`

Pixel color in `0xAARRGGBB` format. Alpha 0xFF.

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