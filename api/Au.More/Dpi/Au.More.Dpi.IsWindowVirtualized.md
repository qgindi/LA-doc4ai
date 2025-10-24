# Method `Au.More.Dpi.IsWindowVirtualized`

Detects whether the window is DPI-scaled/virtualized.

```
public static bool IsWindowVirtualized(wnd w)
```

##### Parameters

- *w*  (`Au.wnd`):
    A top-level window or control. Can belong to any process.

##### Returns

`bool`

`false` if not DPI-scaled/virtualized or if fails to detect or if invalid window handle.

#### Remarks

Such windows are a little blurry (entire client area).

OS scales a window when it is on a high-DPI screen, depending on the DPI awareness of the window:

- Unaware - always.
- System - if the screen DPI is not equal to the system DPI of that process (which usually is of the primary screen, but not always).

Such windows have various problems for automation apps:

- Often difficult or impossible to get correct rectangles of UI elements (and therefore cannot click etc) or get correct UI element from point. It depends on used API (UIA, MSAA, JAB), inproc/notinproc, OS version and application.
- On Windows 7 and 8.0 cannot easily get correct rectangles of such windows and their controls. This library ignores it, because would be too much work to apply workarounds in so many places and just for legacy OS versions (it has been fixed in Windows 8.1).
- If with `Au.uiimage` want to use window pixels, need to capture image from window pixels, not from screen pixels.

This function is not completely reliable. And not very fast. This process must be per-monitor-DPI-aware.