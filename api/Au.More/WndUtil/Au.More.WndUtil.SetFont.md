# Method `Au.More.WndUtil.SetFont`

Sets font.

```
public static void SetFont(wnd w, nint font = 0)
```

##### Parameters

- *w*  (`Au.wnd`)
- *font*  (`nint`):
    Native font handle. If `default(IntPtr)`, sets font that is used by most windows and controls on this computer, usually `Segoe UI` 9, DPI-scaled for *w* screen.

#### Remarks

Sends `WM_SETFONT` message.