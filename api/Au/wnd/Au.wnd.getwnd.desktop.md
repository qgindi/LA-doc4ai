# Method `Au.wnd.getwnd.desktop`

Gets the desktop window and its child control that displays desktop icons and wallpaper.

```
public static bool desktop(out wnd desktopWindow, out wnd control)
```

##### Parameters

- *desktopWindow*  (`Au.wnd`):
    Receives the top-level desktop window. Class name `"Progman"` or `"WorkerW"`.
- *control*  (`Au.wnd`):
    Receives the control of `"SysListView32"` class that contains icons and wallpaper.

##### Returns

`bool`

`false` if failed.

#### Remarks

This function is not very reliable. May stop working on a new Windows version or don't work with a custom shell. Fails if there is no shell process, for example Explorer process killed/crashed and still not restarted, or if using a custom shell that does not register a shell window.