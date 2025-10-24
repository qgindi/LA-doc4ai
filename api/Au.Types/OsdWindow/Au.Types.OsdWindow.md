# Class `Au.Types.OsdWindow`

Transparent window that can be used for on-screen display. Derived classes on it can draw non-transparent text, rectangle, image, anything.

```
public abstract class OsdWindow : IDisposable
```

##### Inheritance

`object` → `OsdWindow`

Derived: `Au.osdRect`, `Au.osdText`

### Properties

`ClickToClose`, `Hwnd`, `IsHandleCreated`, `Name`, `Opacity`, `Rect`, `Shadow`, `TransparentColor`, `Visible`

### Methods

`Close`, `Dispose`, `Dispose`, `Hide`, `Invalidate`, `OnPaint`, `Redraw`, `Show`, `WndProc`, `closeAll`

### Events

`Clicked`, `Closed`