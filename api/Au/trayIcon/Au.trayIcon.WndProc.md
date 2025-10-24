# Method `Au.trayIcon.WndProc`

Window procedure of the hidden window that receives tray icon notifications (`Au.trayIcon.MsgNotify`) in version 4 format. If you override it, call the base function.

```
protected virtual nint WndProc(wnd w, int msg, nint wParam, nint lParam)
```

##### Parameters

- *w*  (`Au.wnd`)
- *msg*  (`int`)
- *wParam*  (`nint`)
- *lParam*  (`nint`)

##### Returns

`nint`