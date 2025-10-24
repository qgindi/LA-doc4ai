# Method `Au.More.CaptureScreen.ImageColorRectUI`

UI for capturing an image, color or rectangle on screen.

```
public static bool ImageColorRectUI(out CIUResult result, CIUFlags flags = 0, AnyWnd owner = default, wnd wCapture = default)
```

##### Parameters

- *result*  (`Au.Types.CIUResult`):
    Receives results.
- *flags*  (`Au.Types.CIUFlags`)
- *owner*  (`Au.Types.AnyWnd`):
    A window to minimize temporarily.
- *wCapture*  (`Au.wnd`):
    A window to capture immediately instead of waiting for `F3` key. Used only with a "get window pixels" flag.

##### Returns

`bool`

`false` if canceled.

#### Remarks

Gets all screen pixels and shows in a full-screen topmost window, where the user can select an area.

Cannot capture windows that are always on top of normal topmost windows: 1. Start menu. 2. Topmost windows of UAC uiAccess processes (rare).