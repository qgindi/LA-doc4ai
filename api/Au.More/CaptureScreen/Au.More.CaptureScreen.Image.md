# Method `Au.More.CaptureScreen.Image`

## Overload 1

Creates image from a rectangle of screen pixels.

```
public static Bitmap Image(RECT r)
```

##### Parameters

- *r*  (`Au.Types.RECT`):
    Rectangle in screen.

##### Returns

`Bitmap`

##### Exceptions

- `ArgumentException`:
    Empty rectangle.
- `Au.Types.AuException`:
    Failed. Probably there is not enough memory for bitmap of this size (`width*height*4` bytes).

#### Examples

```
var file = folders.Temp + "notepad.png";
wnd w = wnd.find("* Notepad");
w.GetRect(out var r, true);
using(var b = CaptureScreen.Image(r)) { b.Save(file); }
run.it(file);
```

* * *

## Overload 2

Creates image from a rectangle of window client area pixels.

```
public static Bitmap Image(wnd w, RECT? r = null, CIFlags flags = CIFlags.WindowDC)
```

##### Parameters

- *w*  (`Au.wnd`):
    Window or control.
- *r*  (`Au.Types.RECT?`):
    Rectangle in *w* client area coordinates. If `null`, uses `w.ClientRect`.
- *flags*  (`Au.Types.CIFlags`)

##### Returns

`Bitmap`

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