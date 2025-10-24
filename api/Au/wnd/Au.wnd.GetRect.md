# Method `Au.wnd.GetRect`

Gets rectangle (position and size) in screen coordinates.

```
public bool GetRect(out RECT r, bool withoutExtendedFrame = false)
```

##### Parameters

- *r*  (`Au.Types.RECT`):
    Receives the rectangle. Will be `default(RECT)` if failed.
- *withoutExtendedFrame*  (`bool`):
    Don't include the transparent part of window border. For it is used API `DwmGetWindowAttribute`(`DWMWA_EXTENDED_FRAME_BOUNDS`); it is less reliable.

##### Returns

`bool`

#### Remarks

The same as the `Au.wnd.Rect` property. Calls API `GetWindowRect` and returns its return value. Supports `Au.lastError`.