# Method `Au.icon.ofWindow`

Gets icon that is displayed in window title bar and in taskbar button.

```
public static icon ofWindow(wnd w, int size = 16)
```

##### Parameters

- *w*  (`Au.wnd`):
    A top-level window of any process.
- *size*  (`int`):
    Icon width and height. Default 16.

##### Returns

`Au.icon`

`null` if failed.