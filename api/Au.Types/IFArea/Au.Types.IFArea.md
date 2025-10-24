# Class `Au.Types.IFArea`

Defines the search area for `Au.uiimage.find` and similar functions.

```
public class IFArea
```

##### Remarks

It can be a window/control, UI element, image or a rectangle in screen. Has implicit conversions from `Au.wnd`, `Au.elm`, `System.Drawing.Bitmap` and `Au.Types.RECT` (rectangle in screen). Constructors can be used to specify a rectangle in window or UI element, which makes the area smaller and the function faster. Example: `uiimage.find(new(w, (left, top, width, height)), image);`.

##### Inheritance

`object` → `IFArea`

### Constructors

`IFArea(elm, Coord, Coord, Coord, Coord)`, `IFArea(elm, RECT)`, `IFArea(wnd, Coord, Coord, Coord, Coord)`, `IFArea(wnd, RECT)`

### Operators

`implicit operator IFArea(RECT)`, `implicit operator IFArea(elm)`, `implicit operator IFArea(wnd)`, `implicit operator IFArea(Bitmap)`