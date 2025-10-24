# Method `Au.mouse.restore`

Moves the mouse cursor where it was at the time of the last `Au.mouse.save`. If it was not called - of the first "mouse move" or "mouse click" function call. Does nothing if these functions were not called.

```
public static void restore()
```

##### Exceptions

- `ArgumentOutOfRangeException`:
    The position is not in screen. No exception if option `Relaxed` is `true` (then moves to a screen edge).
- `Au.Types.AuException`:

    Failed to move the cursor to that position. Some reasons:

    - The active window belongs to a process of higher [UAC](../articles/UAC.html) integrity level.
    - Another thread blocks or modifies mouse input (API `BlockInput`, mouse hooks, frequent API `SendInput` etc).
    - Some application called API `ClipCursor`. No exception if option `Relaxed` is `true` (then final cursor position is undefined).
- `Au.Types.InputDesktopException`

#### Remarks

Uses `Au.opt.mouse`: `Au.Types.OMouse.MoveSleepFinally`, `Au.Types.OMouse.Relaxed`.