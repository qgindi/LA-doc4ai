# Method `Au.wnd.getwnd.nextMain`

Gets next window in the Z order, skipping invisible and other windows that probably are not in the Windows taskbar.

```
public static wnd nextMain(wnd w = default, bool allDesktops = false, bool skipMinimized = false, bool retryFromTop = false)
```

##### Parameters

- *w*  (`Au.wnd`):
    Start from this window. If `default(wnd)`, starts from the top of the Z order.
- *allDesktops*  (`bool`):
    On Windows 10 include windows on all virtual desktops. On Windows 8 include Windows Store apps if possible; read more: `Au.wnd.getwnd.allWindows`.
- *skipMinimized*  (`bool`):
    Skip minimized windows.
- *retryFromTop*  (`bool`):
    If *w* is not `default(wnd)` and there are no matching windows after it, retry from the top of the Z order. Then can return *w*.

##### Returns

`Au.wnd`

`default(wnd)` if there are no such windows.

#### Remarks

Uses `Au.wnd.getwnd.isMainWindow`. This function is quite slow. Does not match the order of buttons in the Windows taskbar.