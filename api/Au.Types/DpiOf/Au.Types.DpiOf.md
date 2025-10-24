# Struct `Au.Types.DpiOf`

Used for *dpiOf* parameter of functions. Allows to pass either a DPI value or an object from which gets DPI (window, screen etc).

```
public struct DpiOf
```

##### Remarks

Has implicit conversions from:

- `int` - DPI.
- `Au.wnd` - gets DPI of the window.
- `IntPtr` or `nint` - (screen handle) gets DPI of the screen.
- `Au.Types.POINT` - gets DPI of the screen that contains the point.
- `Au.Types.RECT` - gets DPI of screen that contains the rectangle.
- `System.Windows.Forms.Control` - gets DPI of the winforms control.
- `System.Windows.DependencyObject` - gets DPI of the WPF element.

The conversion operators set the `Au.Types.DpiOf.Dpi` property and the function can use it.

### Constructors

`DpiOf(POINT)`, `DpiOf(RECT)`, `DpiOf(wnd)`, `DpiOf(int)`, `DpiOf(nint)`, `DpiOf(DependencyObject)`, `DpiOf(Control)`

### Properties

`Dpi`

### Operators

`implicit operator int(DpiOf)`, `implicit operator DpiOf(POINT)`, `implicit operator DpiOf(RECT)`, `implicit operator DpiOf(wnd)`, `implicit operator DpiOf(int)`, `implicit operator DpiOf(nint)`, `implicit operator DpiOf(DependencyObject)`, `implicit operator DpiOf(Control)`