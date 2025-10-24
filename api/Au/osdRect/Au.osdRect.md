# Class `Au.osdRect`

Shows a mouse-transparent rectangle on screen. Just visible outline, or filled but partially transparent.

```
public class osdRect : OsdWindow, IDisposable
```

##### Remarks

Creates a temporary partially transparent window, and draws rectangle in it. Can draw multiple rectangles.

##### Examples

```
using (var x = new osdRect()) {
	x.Rect = (300, 300, 100, 100);
	x.Color = System.Drawing.Color.SlateBlue;
	x.Thickness = 4;
	x.Show();
	for (int i = 0; i < 5; i++) {
		250.ms();
		x.Visible = !x.Visible;
	}
}
```

##### Inheritance

`object` → `Au.Types.OsdWindow` → `osdRect`

### Constructors

`osdRect()`

### Properties

`Color`, `Thickness`

### Methods

`OnPaint`, `SetRects`, `SetRects`

### Members inherited from other types of this library
`OsdWindow.Dispose()`, `OsdWindow.Dispose()`, `OsdWindow.Close()`, `OsdWindow.Hwnd`, `OsdWindow.IsHandleCreated`, `OsdWindow.Redraw()`, `OsdWindow.Invalidate()`, `OsdWindow.Opacity`, `OsdWindow.TransparentColor`, `OsdWindow.Rect`, `OsdWindow.Visible`, `OsdWindow.Show()`, `OsdWindow.Hide()`, `OsdWindow.WndProc()`, `OsdWindow.Closed`, `OsdWindow.Clicked`, `OsdWindow.Shadow`, `OsdWindow.ClickToClose`, `OsdWindow.Name`, `OsdWindow.closeAll()`