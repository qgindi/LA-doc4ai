# Constructor of `Au.More.Dpi.AwarenessContext`

## Overload 1

If `Au.More.Dpi.AwarenessContext.Available`, calls API `SetThreadDpiAwarenessContext`.

```
public AwarenessContext(nint dpiContext)
```

##### Parameters

- *dpiContext*  (`nint`):
    One of `DPI_AWARENESS_CONTEXT` constants: -1 `unaware`, -2 `system`, -3 `per-monitor`, -4 `per-monitor-v2`, -5 `unaware-gdiscaled`. Or a `DPI_AWARENESS_CONTEXT` handle.

* * *

## Overload 2

If `Au.More.Dpi.AwarenessContext.Available`, calls API `GetWindowDpiAwarenessContext` and `SetThreadDpiAwarenessContext`. Sets the awareness context of this thread equal to that of the window.

```
public AwarenessContext(wnd w)
```

##### Parameters

- *w*  (`Au.wnd`)