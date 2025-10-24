# Class `Au.osdText`

Shows text on screen, like a tooltip or with transparent background.

```
public class osdText : OsdWindow, IDisposable
```

##### Remarks

Creates a temporary partially transparent window, and draws text in it. Most properties cannot be changed after creating OSD window.

##### Inheritance

`object` → `Au.Types.OsdWindow` → `osdText`

### Constructors

`osdText()`

### Properties

`BackColor`, `BackgroundImage`, `BorderColor`, `ClickToClose`, `Font`, `Icon`, `IsOfImageSize`, `Rect`, `ResizeWhenContentChanged`, `SecondsTimeout`, `Shadow`, `ShowMode`, `Text`, `TextColor`, `TextFormatFlags`, `WrapWidth`, `XY`, `defaultBackColor`, `defaultBigFont`, `defaultBorderColor`, `defaultScreen`, `defaultSmallFont`, `defaultTextColor`, `defaultTransparentTextColor`

### Methods

`Dispose`, `Measure`, `OnPaint`, `Show`, `WndProc`, `showImage`, `showText`, `showTransparentText`

### Members inherited from other types of this library
`OsdWindow.Dispose()`, `OsdWindow.Close()`, `OsdWindow.Hwnd`, `OsdWindow.IsHandleCreated`, `OsdWindow.Redraw()`, `OsdWindow.Invalidate()`, `OsdWindow.Opacity`, `OsdWindow.TransparentColor`, `OsdWindow.Visible`, `OsdWindow.Hide()`, `OsdWindow.Closed`, `OsdWindow.Clicked`, `OsdWindow.Name`, `OsdWindow.closeAll()`