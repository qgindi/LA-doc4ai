# Method `Au.wnd.switchActiveWindow`

Activates next non-minimized main window, like with `Alt+Tab`.

```
public static bool switchActiveWindow()
```

##### Returns

`bool`

`true` if activated; `false` if there is no such window or if failed to activate.

#### Remarks

Uses `Au.wnd.getwnd.nextMain`, `Au.wnd.getwnd.LastActiveOwnedOrThis`, `Au.wnd.Activate`. An alternative way - send `Alt+Tab` keys, but it works not everywhere.