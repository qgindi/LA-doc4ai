# Method `Au.miscInfo.getTextCursorRect`

Gets caret rectangle.

```
public static bool getTextCursorRect(out RECT r, out wnd w, bool orMouse = false)
```

##### Parameters

- *r*  (`Au.Types.RECT`):
    Receives the rectangle, in screen coordinates.
- *w*  (`Au.wnd`):
    Receives the caret owner control or the focused control.
- *orMouse*  (`bool`):
    If fails, get mouse pointer coordinates.

##### Returns

`bool`

`false` if failed.

#### Remarks

Some apps use non-standard caret; then may fail.