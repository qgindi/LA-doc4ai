# Method `Au.mouse.clickEx`

## Overload 1

Clicks, double-clicks, presses or releases a mouse button at position *x y* relative to window *w*.

```
public static MRelease clickEx(MButton button, wnd w, Coord x = default, Coord y = default, bool nonClient = false)
```

##### Parameters

- *button*  (`Au.Types.MButton`):
    Button and action. Default: left click.
- *w*  (`Au.wnd`):
    Window or control.
- *x*  (`Au.Types.Coord`):
    X coordinate relative to the client area of *w*. Default - center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate relative to the client area of *w*. Default - center.
- *nonClient*  (`bool`):
    The specified position is relative to the window rectangle, not to its client area.

##### Returns

`Au.Types.MRelease`

The return value can be used to auto-release the pressed button. Example: `Au.Types.MRelease`.

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

#### Remarks

To move the mouse cursor, calls `Au.mouse.move`. If after moving the cursor it is not in the window (or a window of its thread), activates the window (or its top-level parent window). Throws exception if then *x y* is still not in the window. Skips all this when just releasing button or if option `Relaxed` is `true`. If *w* is a control, *x y* can be somewhere else in its top-level parent window.

Uses `Au.opt.mouse`: `Au.Types.OMouse.MoveSpeed`, `Au.Types.OMouse.MoveSleepFinally` (between moving and clicking), `Au.Types.OMouse.ClickSpeed`, `Au.Types.OMouse.ClickSleepFinally`, `Au.Types.OMouse.Relaxed`.

#### Examples

```
mouse.clickEx(MButton.Middle, w1, 695, 110);
mouse.clickEx(MButton.Right | MButton.Down, w1, 695, 110);
mouse.clickEx(MButton.Right | MButton.Up, w1, 695, 110);
```

* * *

## Overload 2

Clicks, double-clicks, presses or releases a mouse button at position *x y* relative to UI object *obj*.

```
public static MRelease clickEx(MButton button, MObject obj, Coord x = default, Coord y = default)
```

##### Parameters

- *button*  (`Au.Types.MButton`):
    Button and action. Default: left click.
- *obj*  (`Au.Types.MObject`):
    Can be `Au.wnd`, `Au.elm` (`Au.elm.MouseClick`), `Au.uiimage` (`Au.uiimage.MouseClick`), `Au.screen`, `Au.Types.RECT` in screen, `Au.Types.RECT` in window, `Au.mouse.lastXY` (`true`), `Au.mouse.xy` (`false`).
- *x*  (`Au.Types.Coord`):
    X coordinate relative to *obj*. Default - center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate relative to *obj*. Default - center.

##### Returns

`Au.Types.MRelease`

The return value can be used to auto-release the pressed button. Example: `Au.Types.MRelease`.

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

#### Remarks

To move the mouse cursor, calls `Au.mouse.move`. If after moving the cursor it is not in the window (or a window of its thread), activates the window (or its top-level parent window). Throws exception if then *x y* is still not in the window. Skips all this when just releasing button or if option `Relaxed` is `true`. If *w* is a control, *x y* can be somewhere else in its top-level parent window.

Uses `Au.opt.mouse`: `Au.Types.OMouse.MoveSpeed`, `Au.Types.OMouse.MoveSleepFinally` (between moving and clicking), `Au.Types.OMouse.ClickSpeed`, `Au.Types.OMouse.ClickSleepFinally`, `Au.Types.OMouse.Relaxed`.

* * *

## Overload 3

Clicks, double-clicks, presses or releases a mouse button at the specified position in screen.

```
public static MRelease clickEx(MButton button, Coord x, Coord y)
```

##### Parameters

- *button*  (`Au.Types.MButton`):
    Button and action. Default: left click.
- *x*  (`Au.Types.Coord`):
    X coordinate in the screen. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate in the screen.

##### Returns

`Au.Types.MRelease`

The return value can be used to auto-release the pressed button. Example: `Au.Types.MRelease`.

##### Exceptions

- `ArgumentException`:
    Invalid *button* flags (multiple buttons or actions specified).
- `ArgumentOutOfRangeException`:
    The position is not in screen. No exception if option `Relaxed` is `true` (then moves to a screen edge).
- `Au.Types.AuException`:

    Failed to move the cursor to that position. Some reasons:

    - The active window belongs to a process of higher [UAC](../articles/UAC.html) integrity level.
    - Another thread blocks or modifies mouse input (API `BlockInput`, mouse hooks, frequent API `SendInput` etc).
    - Some application called API `ClipCursor`. No exception if option `Relaxed` is `true` (then final cursor position is undefined).
- `Au.Types.InputDesktopException`

#### Remarks

Uses `Au.opt.mouse`: `Au.Types.OMouse.ClickSpeed`, `Au.Types.OMouse.ClickSleepFinally` and those used by `Au.mouse.move`.

* * *

## Overload 4

Clicks, double-clicks, presses or releases a mouse button at the specified position in screen.

```
public static MRelease clickEx(MButton button, POINT p)
```

##### Parameters

- *button*  (`Au.Types.MButton`):
    Button and action. Default: left click.
- *p*  (`Au.Types.POINT`):
    Coordinates. Tip: To specify coordinates relative to the right, bottom, work area or a non-primary screen, use `Au.Types.Coord.Normalize`, like in the example.

##### Returns

`Au.Types.MRelease`

The return value can be used to auto-release the pressed button. Example: `Au.Types.MRelease`.

##### Exceptions

- `ArgumentException`:
    Invalid *button* flags (multiple buttons or actions specified).
- `ArgumentOutOfRangeException`:
    The position is not in screen. No exception if option `Relaxed` is `true` (then moves to a screen edge).
- `Au.Types.AuException`:

    Failed to move the cursor to that position. Some reasons:

    - The active window belongs to a process of higher [UAC](../articles/UAC.html) integrity level.
    - Another thread blocks or modifies mouse input (API `BlockInput`, mouse hooks, frequent API `SendInput` etc).
    - Some application called API `ClipCursor`. No exception if option `Relaxed` is `true` (then final cursor position is undefined).
- `Au.Types.InputDesktopException`

#### Remarks

Uses `Au.opt.mouse`: `Au.Types.OMouse.ClickSpeed`, `Au.Types.OMouse.ClickSleepFinally` and those used by `Au.mouse.move`.

#### Examples

Click at 100 200.

```
mouse.clickEx(MButton.Left, (100, 200));
```

Right-click at 50 from left and 100 from bottom of the work area.

```
mouse.clickEx(MButton.Right, Coord.Normalize(50, ^100, workArea: true));
```

* * *

## Overload 5

Clicks, double-clicks, presses or releases a mouse button. By default does not move the mouse cursor.

```
public static MRelease clickEx(MButton button = MButton.Left, bool useLastXY = false)
```

##### Parameters

- *button*  (`Au.Types.MButton`):
    Button and action. Default: left click.
- *useLastXY*  (`bool`):
    Use `Au.mouse.lastXY`. It is the mouse cursor position set by the most recent "mouse move" or "mouse click" function. Use this option for reliability. Example: `mouse.move(100, 100); mouse.clickEx(..., true);`. The click is always at 100 100, even if somebody changes cursor position between `mouse.move` sets it and `mouse.clickEx` uses it. In such case this option atomically moves the cursor to `Au.mouse.lastXY`. This movement is instant and does not use `Au.opt`. If `false` (default), clicks at the current cursor position (does not move it).

##### Returns

`Au.Types.MRelease`

The return value can be used to auto-release the pressed button. Example: `Au.Types.MRelease`.

##### Exceptions

- `ArgumentException`:
    Invalid *button* flags (multiple buttons or actions specified).
- `Exception`:
    If *lastXY* `true` and need to move the cursor - exceptions of `Au.mouse.move`.
- `Au.Types.InputDesktopException`

#### Remarks

Uses `Au.opt.mouse`: `Au.Types.OMouse.ClickSpeed`, `Au.Types.OMouse.ClickSleepFinally` and maybe those used by `Au.mouse.move`.