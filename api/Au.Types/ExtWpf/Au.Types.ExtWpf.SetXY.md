# Method `Au.Types.ExtWpf.SetXY`

Sets window startup location before showing it first time. Also can move already loaded window.

```
public static void SetXY(this Window t, int x, int y)
```

##### Parameters

- *t*  (`Window`)
- *x*  (`int`):
    X coordinate in screen. Physical pixels.
- *y*  (`int`):
    Y coordinate in screen. Physical pixels.

#### Remarks

The unit is physical pixels. WPF provides `Left` and `Top` properties, but the unit is logical pixels, therefore cannot set exact location on high DPI screens, especially if there are multiple screens with different DPI.

If the window is already loaded, just ensures it is not maximized/minimized and calls `Au.wnd.MoveL`.

Else sets window location for normal state (not minimized/maximized). Temporarily changes `Title`. Clears `WindowStartupLocation`, `Left`, `Top`. Clears `ShowActivated` if minimized. Does not change `SizeToContent`.