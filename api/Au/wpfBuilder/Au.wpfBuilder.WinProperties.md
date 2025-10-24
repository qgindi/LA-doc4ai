# Method `Au.wpfBuilder.WinProperties`

Changes various window properties.

```
public wpfBuilder WinProperties(WindowStartupLocation? startLocation = null, ResizeMode? resizeMode = null, bool? showActivated = null, bool? showInTaskbar = null, bool? topmost = null, WindowState? state = null, WindowStyle? style = null, ImageSource icon = null, bool? whiteBackground = null)
```

##### Parameters

- *startLocation*  (`WindowStartupLocation?`):
    Sets `System.Windows.WindowStartupLocation`.
- *resizeMode*  (`ResizeMode?`):
    Sets `System.Windows.Window.ResizeMode`.
- *showActivated*  (`bool?`):
    Sets `System.Windows.Window.ShowActivated`.
- *showInTaskbar*  (`bool?`):
    Sets `System.Windows.Window.ShowInTaskbar`.
- *topmost*  (`bool?`):
    Sets `System.Windows.Window.Topmost`.
- *state*  (`WindowState?`):
    Sets `System.Windows.Window.WindowState`.
- *style*  (`WindowStyle?`):
    Sets `System.Windows.Window.WindowStyle`.
- *icon*  (`ImageSource`):
    Sets `System.Windows.Window.Icon`. Example: `.WinProperties(icon: BitmapFrame.Create(new Uri(@"d:\icons\file.ico")))`.
- *whiteBackground*  (`bool?`):
    Set background color: `true` `System.Windows.SystemColors.WindowBrush` (white), `false` `System.Windows.SystemColors.ControlBrush` (gray). See also `Au.wpfBuilder.winWhite`, `Au.wpfBuilder.Brush`.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `InvalidOperationException`:

    - Container is not of type `Window`.
    - *startLocation* or *state* used after `Au.wpfBuilder.WinXY`, `Au.wpfBuilder.WinRect` or `Au.wpfBuilder.WinSaved`.

#### Remarks

The function uses only non-`null` parameters. Or you can change `Au.wpfBuilder.Window` properties directly, for example `b.Window.Topmost = true;`.