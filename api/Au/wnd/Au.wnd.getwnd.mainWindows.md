# Method `Au.wnd.getwnd.mainWindows`

Gets main windows, ie those that probably are in the Windows taskbar.

```
public static wnd[] mainWindows(bool allDesktops = false)
```

##### Parameters

- *allDesktops*  (`bool`):
    On Windows 10 include windows on all virtual desktops. On Windows 8 include Windows Store apps if possible; read more: `Au.wnd.getwnd.allWindows`.

##### Returns

`Au.wnd[]`

Array containing zero or more `Au.wnd`.

#### Remarks

Uses `Au.wnd.getwnd.isMainWindow`. Does not match the order of buttons in the Windows taskbar.