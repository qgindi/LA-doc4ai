# Method `Au.wnd.getwnd.isMainWindow`

Returns `true` if window *w* is considered a main window, ie probably is in the Windows taskbar. Returns `false` if it is invisible, cloaked, owned, toolwindow, menu, etc.

```
public static bool isMainWindow(wnd w, bool allDesktops = false, bool skipMinimized = false)
```

##### Parameters

- *w*  (`Au.wnd`):
    A top-level window.
- *allDesktops*  (`bool`):
    On Windows 10 include (return `true` for) windows on all virtual desktops. On Windows 8 include Windows Store apps if possible; read more: `Au.wnd.getwnd.allWindows`.
- *skipMinimized*  (`bool`):
    Return `false` if *w* is minimized.

##### Returns

`bool`