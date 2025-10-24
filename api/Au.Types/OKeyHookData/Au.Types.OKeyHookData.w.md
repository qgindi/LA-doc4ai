# Field `Au.Types.OKeyHookData.w`

The focused control. If there is no focused control - the active window. Use `w.Window` to get top-level window; if `w.Window == w`, `w` is the active window, else the focused control. The callback function is not called if there is no active window.

```
public readonly wnd w
```