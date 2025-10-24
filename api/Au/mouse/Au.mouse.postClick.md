# Method `Au.mouse.postClick`

Posts mouse-click messages to the window.

```
public static void postClick(wnd w, Coord x = default, Coord y = default, MButton button = MButton.Left, RECT? rect = null)
```

##### Parameters

- *w*  (`Au.wnd`):
    Window or control.
- *x*  (`Au.Types.Coord`):
    X coordinate in *w* client area or *rect*. Default - center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate in *w* client area or *rect*. Default - center.
- *button*  (`Au.Types.MButton`):
    Can specify the left (default), right or middle button. Also flag for double-click, press or release.
- *rect*  (`Au.Types.RECT?`):
    A rectangle in *w* client area. If `null` (default), *x y* are relative to the client area.

##### Exceptions

- `Au.Types.AuWndException`:
    Invalid window.
- `ArgumentException`:
    Unsupported button specified.

#### Remarks

Does not move the mouse. Does not wait until the target application finishes processing the message. Works not with all windows.