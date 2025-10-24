# Method `Au.Types.OsdWindow.WndProc`

Called when the OSD window receives a message. If your derived class overrides this function, it must call `base.WndProc` and return its return value, except when don't need default processing.

```
protected virtual nint WndProc(wnd w, int message, nint wParam, nint lParam)
```

##### Parameters

- *w*  (`Au.wnd`)
- *message*  (`int`)
- *wParam*  (`nint`)
- *lParam*  (`nint`)

##### Returns

`nint`