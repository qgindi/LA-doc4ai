# Constructor of `Au.trayIcon`

```
public trayIcon(int id = 0, bool disposeOnExit = true)
```

##### Parameters

- *id*  (`int`):
    An id that helps Windows to distinguish multiple tray icons added by same program. Use 0, 1, 2, ... or all 0.
- *disposeOnExit*  (`bool`):
    Remove tray icon when process exits (`Au.process.thisProcessExit`). Note: can't remove if the process terminated or called `System.Environment.FailFast` or API `ExitProcess`.