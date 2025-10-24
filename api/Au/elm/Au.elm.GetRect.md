# Method `Au.elm.GetRect`

## Overload 1

Gets location of this UI element in screen.

```
public bool GetRect(out RECT r, bool raw = false)
```

##### Parameters

- *r*  (`Au.Types.RECT`):
    Rectangle in screen coordinates.
- *raw*  (`bool`):
    Don't DPI-scale. When the element is in a DPI-scaled/virtualized window (see `Au.More.Dpi.IsWindowVirtualized`), the raw rectangle may not match the visible rectangle. This parameter is ignored on Windows 7 and 8.0 or if this element was retrieved not in-process.

##### Returns

`bool`

`false` if failed or this property is unavailable. Supports `Au.lastError`.

#### Remarks

Most but not all UI elements support this property.

* * *

## Overload 2

Gets location of this UI element in the client area of window *w*.

```
public bool GetRect(out RECT r, wnd w, bool intersect = false)
```

##### Parameters

- *r*  (`Au.Types.RECT`):
    Receives rectangle in *w* client area coordinates.
- *w*  (`Au.wnd`):
    Window or control.
- *intersect*  (`bool`):
    Intersect the rectangle with the *w* client area, possibly making it smaller or empty.

##### Returns

`bool`

`false` if failed or this property is unavailable. Supports `Au.lastError`.

#### Remarks

Most but not all UI elements support this property. Uses `Au.elm.GetRect(out RECT, bool)` and `Au.wnd.MapScreenToClient`.