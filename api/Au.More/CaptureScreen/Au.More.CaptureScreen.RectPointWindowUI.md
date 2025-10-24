# Method `Au.More.CaptureScreen.RectPointWindowUI`

UI for capturing a rectangle, point or/and window on screen with `Shift` key.

```
public static bool RectPointWindowUI(out CRUResult result, CRUType type, bool rectInClient = false, WXYFlags wxyFlags = 0)
```

##### Parameters

- *result*  (`Au.Types.CRUResult`)
- *type*  (`Au.Types.CRUType`)
- *rectInClient*  (`bool`):
    Get rectangle in window client area.
- *wxyFlags*  (`Au.Types.WXYFlags`)

##### Returns

`bool`

`true` if captured, `false` if pressed `Esc`.