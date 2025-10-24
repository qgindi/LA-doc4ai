# Method `Au.mouse.click`

## Overload 1

Left button click at position *x y* relative to window *w*.

```
public static void click(wnd w, Coord x = default, Coord y = default, bool nonClient = false)
```

##### Parameters

- *w*  (`Au.wnd`):
    Window or control.
- *x*  (`Au.Types.Coord`):
    X coordinate relative to the client area of *w*. Default - center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate relative to the client area of *w*. Default - center.
- *nonClient*  (`bool`):
    The specified position is relative to the window rectangle, not to its client area.

##### Exceptions

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

* * *

## Overload 2

Left button click at position *x y*.

```
public static void click(Coord x, Coord y)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X coordinate in the screen. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate in the screen.

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

Uses `Au.opt.mouse`: `Au.Types.OMouse.ClickSpeed`, `Au.Types.OMouse.ClickSleepFinally` and those used by `Au.mouse.move`.

* * *

## Overload 3

Left button click.

```
public static void click(bool useLastXY = false)
```

##### Parameters

- *useLastXY*  (`bool`):
    Use `Au.mouse.lastXY`, not current cursor position. More info: `Au.mouse.clickEx`.

##### Exceptions

- `Exception`:
    If *lastXY* `true` and need to move the cursor - exceptions of `Au.mouse.move`.
- `Au.Types.InputDesktopException`

#### Remarks

Uses `Au.opt.mouse`: `Au.Types.OMouse.ClickSpeed`, `Au.Types.OMouse.ClickSleepFinally` and maybe those used by `Au.mouse.move`.