# Method `Au.mouse.moveBy`

## Overload 1

Moves the cursor (mouse pointer) relative to `Au.mouse.lastXY` or `Au.mouse.xy`.

```
public static POINT moveBy(int dx, int dy, bool useLastXY = true)
```

##### Parameters

- *dx*  (`int`):
    X offset from `lastXY.x` or `xy.x`.
- *dy*  (`int`):
    Y offset from `lastXY.y` or `xy.y`.
- *useLastXY*  (`bool`):
    If `true` (default), moves relative to `Au.mouse.lastXY`, else relative to `Au.mouse.xy`.

##### Returns

`Au.Types.POINT`

Final cursor position in screen.

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

Uses `Au.opt.mouse`: `Au.Types.OMouse.MoveSpeed`, `Au.Types.OMouse.MoveSleepFinally`, `Au.Types.OMouse.Relaxed`.

* * *

## Overload 2

Moves the cursor (mouse pointer) relative to `Au.mouse.lastXY`. Uses multiple x y offsets.

```
public static POINT moveBy(string offsets, double speedFactor = 1)
```

##### Parameters

- *offsets*  (`string`):
    String containing multiple x y offsets. Created by a mouse recorder tool with `Au.More.RecordingUtil.MouseToString`.
- *speedFactor*  (`double`):
    Speed factor. For example, 0.5 makes 2 times faster.

##### Returns

`Au.Types.POINT`

Final cursor position in screen.

##### Exceptions

- `FormatException`:
    Invalid Base64 string.
- `ArgumentException`:
    The string is not compatible with this library version (recorded with a newer version and has additional options).
- `ArgumentOutOfRangeException`:
    The position is not in screen. No exception if option `Relaxed` is `true` (then moves to a screen edge).
- `Au.Types.AuException`:

    Failed to move the cursor to that position. Some reasons:

    - The active window belongs to a process of higher [UAC](../articles/UAC.html) integrity level.
    - Another thread blocks or modifies mouse input (API `BlockInput`, mouse hooks, frequent API `SendInput` etc).
    - Some application called API `ClipCursor`. No exception if option `Relaxed` is `true` (then final cursor position is undefined).
- `Au.Types.InputDesktopException`

#### Remarks

Uses `Au.opt.mouse`: `Au.Types.OMouse.Relaxed` (only for the last movement; always relaxed in intermediate movements).