# Method `Au.More.Dpi.OfWindow`

## Overload 1

Gets the DPI of a window, as used in the window's process. It never changes for that window instance.

```
public static int OfWindow(wnd w, bool supportWin81 = false)
```

##### Parameters

- *w*  (`Au.wnd`):
    A top-level window or control. Can belong to any process.
- *supportWin81*  (`bool`):
    If `true`, works on Windows 8.1 and later; however on Windows 8.1 slower and less reliable. If `false` (default), works on Windows 10 1607 and later.

##### Returns

`int`

If failed, returns the system DPI (`Au.More.Dpi.System`).

#### Remarks

The result depends on the DPI awareness of the window:

- per-monitor-DPI-aware - usually DPI of the windows's screen.
- system aware - system DPI (DPI of the primary screen).
- unaware - 96.

The result also depends on the Windows version:

- Works best on Windows 10 1607 and later. Uses API `GetDpiForWindow`.
- On Windows 8.1 works if *supportWin81* `true`. If `false` (default), returns `Au.More.Dpi.System`.
- On Windows 7 and 8.0 always returns `Au.More.Dpi.System`, because there are no Windows API. Most apps are system-DPI-aware and the result is correct; for unaware apps the result is incorrect. These Windows versions don't support per-monitor DPI.

* * *

## Overload 2

Returns `OfWindow(w.Hwnd())`.

```
public static int OfWindow(Control w)
```

##### Parameters

- *w*  (`Control`):
    A Winforms window or control.

##### Returns

`int`

* * *

## Overload 3

Returns `OfWindow(w.Hwnd())`.

```
public static int OfWindow(DependencyObject w)
```

##### Parameters

- *w*  (`DependencyObject`):
    A WPF window or element.

##### Returns

`int`