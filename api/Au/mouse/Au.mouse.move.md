# Method `Au.mouse.move`

## Overload 1

Moves the cursor (mouse pointer) to the position *x y* relative to window *w*.

```
public static POINT move(wnd w, Coord x = default, Coord y = default, bool nonClient = false)
```

##### Parameters

- *w*  (`Au.wnd`):
    Window or control.
- *x*  (`Au.Types.Coord`):
    X coordinate relative to the client area of *w*. Default - center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate relative to the client area of *w*. Default - center.
- *nonClient*  (`bool`):
    *x y* are relative to the window rectangle.

##### Returns

`Au.Types.POINT`

Cursor position in screen coordinates.

##### Exceptions

- `Au.Types.AuWndException`:

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

#### Remarks

Uses `Au.opt.mouse`: `Au.Types.OMouse.MoveSpeed`, `Au.Types.OMouse.MoveSleepFinally`, `Au.Types.OMouse.Relaxed`.

* * *

## Overload 2

Moves the cursor (mouse pointer) to the position *x y* relative to UI object *obj*.

```
public static void move(MObject obj, Coord x = default, Coord y = default)
```

##### Parameters

- *obj*  (`Au.Types.MObject`):
    Can be `Au.wnd`, `Au.elm`, `Au.uiimage`, `Au.screen`, `Au.Types.RECT` in screen, `Au.Types.RECT` in window, `Au.mouse.lastXY` (`true`), `Au.mouse.xy` (`false`)
- *x*  (`Au.Types.Coord`):
    X coordinate relative to *obj*. Default - center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate relative to *obj*. Default - center.

##### Exceptions

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

#### Remarks

Uses `Au.opt.mouse`: `Au.Types.OMouse.MoveSpeed`, `Au.Types.OMouse.MoveSleepFinally`, `Au.Types.OMouse.Relaxed`.

* * *

## Overload 3

Moves the cursor (mouse pointer) to the specified position in screen.

```
public static POINT move(Coord x, Coord y)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X coordinate. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate.

##### Returns

`Au.Types.POINT`

Normalized cursor position.

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

## Overload 4

Moves the cursor (mouse pointer) to the specified position in screen.

```
public static void move(POINT p)
```

##### Parameters

- *p*  (`Au.Types.POINT`):
    Coordinates. Tip: To specify coordinates relative to the right, bottom, work area or a non-primary screen, use `Au.Types.Coord.Normalize`, like in the example.

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

#### Examples

Save-restore mouse position.

```
var p = mouse.xy;
//...
mouse.move(p);
```

Use coordinates in the first non-primary screen.

```
mouse.move(Coord.Normalize(10, ^10, screen: screen.index(1))); //10 from left, 10 from bottom
```