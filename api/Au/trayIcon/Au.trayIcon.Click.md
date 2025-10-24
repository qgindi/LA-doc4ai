# Event `Au.trayIcon.Click`

When default action should be invoked (on click, `Space`/`Enter`, automation/accessibility API).

```
public event Action<TIEventArgs> Click
```

#### **Remarks**

If clicked, the parameter contains message `NIN_SELECT` (1024) and mouse coordinates. Else `NIN_KEYSELECT` (1025) and top-left of the tray icon. On double click there are two `Click` events. To distinguish click and double click events, use `Au.trayIcon.Message` instead.