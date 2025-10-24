# Method `Au.mouse.drag`

## Overload 1

Presses a mouse button in object *o1*, moves the mouse cursor to object *o2* and releases the button.

```
public static void drag(MObject o1, MObject o2, Coord x1 = default, Coord y1 = default, Coord x2 = default, Coord y2 = default, MButton button = MButton.Left, KMod mod = 0, int sleep = 0, int speed = 5)
```

##### Parameters

- *o1*  (`Au.Types.MObject`):
    UI object (window, UI element, etc) where to press the mouse button.
- *o2*  (`Au.Types.MObject`):
    UI object where to release the mouse button.
- *x1*  (`Au.Types.Coord`):
    X offset in *o1* rectangle. Default: center.
- *y1*  (`Au.Types.Coord`):
    Y offset in *o1* rectangle. Default: center.
- *x2*  (`Au.Types.Coord`):
    X offset in *o2* rectangle. Default: center.
- *y2*  (`Au.Types.Coord`):
    Y offset in *o2* rectangle. Default: center.
- *button*  (`Au.Types.MButton`):
    Mouse button. Default: left.
- *mod*  (`Au.Types.KMod`):
    Modifier keys (`Ctrl` etc).
- *sleep*  (`int`):
    Wait this number of milliseconds after pressing the mouse button.
- *speed*  (`int`):
    The drag speed. See `Au.Types.OMouse.MoveSpeed`.

##### Exceptions

- `ArgumentException`:
    Invalid *button* flags (multiple buttons or actions specified).
- `Au.Types.AuWndException`:

    - The specified position is not in the window (read more in Remarks).
    - Invalid window.
    - The window is hidden. No exception if just cloaked, for example in another desktop; then on click will activate, which usually uncloaks. No exception if *w* is a control.
    - Other window-related failures.
- `ArgumentOutOfRangeException`:
    The position is not in screen. No exception if option `Relaxed` is `true` (then moves to a screen edge).
- `Au.Types.AuException`:

    Failed to move the cursor to that position. Some reasons:

    - The active window belongs to a process of higher [UAC](../articles/UAC.html) integrity level.
    - Another thread blocks or modifies mouse input (API `BlockInput`, mouse hooks, frequent API `SendInput` etc).
    - Some application called API `ClipCursor`. No exception if option `Relaxed` is `true` (then final cursor position is undefined).
- `Au.Types.InputDesktopException`
- `Exception`:
    Other exceptions. Depends on *obj* type.

* * *

## Overload 2

Presses a mouse button in object *obj*, moves the mouse cursor by offset *dx* *dy* and releases the button.

```
public static void drag(MObject obj, Coord x, Coord y, int dx, int dy, MButton button = MButton.Left, KMod mod = 0, int sleep = 0, int speed = 5)
```

##### Parameters

- *obj*  (`Au.Types.MObject`):
    UI object (window, UI element, etc) where to press the mouse button.
- *x*  (`Au.Types.Coord`):
    X offset in *obj* rectangle. Default: center.
- *y*  (`Au.Types.Coord`):
    Y offset in *obj* rectangle. Default: center.
- *dx*  (`int`):
    X offset from the start position.
- *dy*  (`int`):
    Y offset from the start position.
- *button*  (`Au.Types.MButton`):
    Mouse button. Default: left.
- *mod*  (`Au.Types.KMod`):
    Modifier keys (`Ctrl` etc).
- *sleep*  (`int`):
    Wait this number of milliseconds after pressing the mouse button.
- *speed*  (`int`):
    The drag speed. See `Au.Types.OMouse.MoveSpeed`.

##### Exceptions

- `ArgumentException`:
    Invalid *button* flags (multiple buttons or actions specified).
- `Au.Types.AuWndException`:

    - The specified position is not in the window (read more in Remarks).
    - Invalid window.
    - The window is hidden. No exception if just cloaked, for example in another desktop; then on click will activate, which usually uncloaks. No exception if *w* is a control.
    - Other window-related failures.
- `ArgumentOutOfRangeException`:
    The position is not in screen. No exception if option `Relaxed` is `true` (then moves to a screen edge).
- `Au.Types.AuException`:

    Failed to move the cursor to that position. Some reasons:

    - The active window belongs to a process of higher [UAC](../articles/UAC.html) integrity level.
    - Another thread blocks or modifies mouse input (API `BlockInput`, mouse hooks, frequent API `SendInput` etc).
    - Some application called API `ClipCursor`. No exception if option `Relaxed` is `true` (then final cursor position is undefined).
- `Au.Types.InputDesktopException`
- `Exception`:
    Other exceptions. Depends on *obj* type.

* * *

## Overload 3

Presses a mouse button in object *obj*, moves the mouse cursor using multiple recorded offsets and releases the button.

```
public static void drag(MObject obj, Coord x, Coord y, string offsets, MButton button = MButton.Left, KMod mod = 0, int sleep = 0)
```

##### Parameters

- *obj*  (`Au.Types.MObject`):
    UI object (window, UI element, etc) where to press the mouse button.
- *x*  (`Au.Types.Coord`):
    X offset in *obj* rectangle. Default: center.
- *y*  (`Au.Types.Coord`):
    Y offset in *obj* rectangle. Default: center.
- *offsets*  (`string`):
    String containing multiple x y offsets from the start position. See `Au.mouse.moveBy`.
- *button*  (`Au.Types.MButton`):
    Mouse button. Default: left.
- *mod*  (`Au.Types.KMod`):
    Modifier keys (`Ctrl` etc).
- *sleep*  (`int`):
    Wait this number of milliseconds after pressing the mouse button.

##### Exceptions

- `ArgumentException`:
    Invalid *button* flags (multiple buttons or actions specified).
- `Au.Types.AuWndException`:

    - The specified position is not in the window (read more in Remarks).
    - Invalid window.
    - The window is hidden. No exception if just cloaked, for example in another desktop; then on click will activate, which usually uncloaks. No exception if *w* is a control.
    - Other window-related failures.
- `ArgumentOutOfRangeException`:
    The position is not in screen. No exception if option `Relaxed` is `true` (then moves to a screen edge).
- `Au.Types.AuException`:

    Failed to move the cursor to that position. Some reasons:

    - The active window belongs to a process of higher [UAC](../articles/UAC.html) integrity level.
    - Another thread blocks or modifies mouse input (API `BlockInput`, mouse hooks, frequent API `SendInput` etc).
    - Some application called API `ClipCursor`. No exception if option `Relaxed` is `true` (then final cursor position is undefined).
- `Au.Types.InputDesktopException`
- `Exception`:
    Other exceptions. Depends on *obj* type.