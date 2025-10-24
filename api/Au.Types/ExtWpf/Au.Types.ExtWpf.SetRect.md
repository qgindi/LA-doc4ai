# Method `Au.Types.ExtWpf.SetRect`

Sets window startup rectangle (location and size) before showing it first time. Also can move/resize already loaded window.

```
public static void SetRect(this Window t, RECT r)
```

##### Parameters

- *t*  (`Window`)
- *r*  (`Au.Types.RECT`):
    Rectangle in screen. Physical pixels.

#### Remarks

The unit is physical pixels. WPF provides `Left`, `Top`, `Width` and `Height` properties, but the unit is logical pixels, therefore cannot set exact rectangle on high DPI screens, especially if there are multiple screens with different DPI.

If the window is already loaded, just ensures it is not maximized/minimized and calls `Au.wnd.MoveL`.

Else sets window rectangle for normal state (not minimized/maximized). Temporarily changes `Title`. Clears `WindowStartupLocation`, `Left`, `Top`, `Width`, `Height`. Clears `ShowActivated` if minimized. Does not change `SizeToContent`.