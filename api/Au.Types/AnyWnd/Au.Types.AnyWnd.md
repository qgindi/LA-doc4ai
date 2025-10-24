# Struct `Au.Types.AnyWnd`

Used for parameters of functions that need a window handle as `Au.wnd` but also accept a WPF window/element, winforms form/control and `IntPtr`.

```
public struct AnyWnd
```

##### Remarks

Has implicit conversions from:

- `System.Windows.DependencyObject` - WPF window or element.
- `System.Windows.Forms.Control` - `Form` or control.
- `IntPtr` or `nint` - window handle.

### Properties

`Hwnd`, `IsEmpty`

### Operators

`implicit operator AnyWnd(wnd)`, `implicit operator AnyWnd(nint)`, `implicit operator AnyWnd(DependencyObject)`, `implicit operator AnyWnd(Control)`