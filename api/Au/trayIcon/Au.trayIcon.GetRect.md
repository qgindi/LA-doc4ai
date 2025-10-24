# Method `Au.trayIcon.GetRect`

Gets tray icon rectangle in screen.

```
public bool GetRect(out RECT r)
```

##### Parameters

- *r*  (`Au.Types.RECT`)

##### Returns

`bool`

`false` if failed, for example if the icon is in hidden overflow area. Supports `Au.lastError`.