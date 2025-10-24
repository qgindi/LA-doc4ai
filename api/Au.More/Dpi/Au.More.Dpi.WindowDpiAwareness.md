# Method `Au.More.Dpi.WindowDpiAwareness`

Gets DPI awareness of a window.

```
public static Dpi.Awareness WindowDpiAwareness(wnd w)
```

##### Parameters

- *w*  (`Au.wnd`):
    A top-level window or control. Can belong to any process.

##### Returns

`Au.More.Dpi`.`Au.More.Dpi.Awareness`

`Au.More.Dpi.Awareness.Invalid` if failed.

#### Remarks

Works best on Windows 10 1607 and later; uses API `GetWindowDpiAwarenessContext`. On Windows 8.1 returns `Au.More.Dpi.Awareness.PerMonitor` if *w* is of this process; else uses API `GetProcessDpiAwareness`, which is slower and less reliable. On Windows 7 and 8.0 always returns `Au.More.Dpi.Awareness.System`, because there are no Windows API.