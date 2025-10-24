# Method `Au.More.WndUtil.EnableActivate`

Temporarily enables this process to activate windows with API `SetForegroundWindow`.

```
public static bool EnableActivate(int processId = 0)
```

##### Parameters

- *processId*  (`int`):
    Process id. If not 0, enables that process to activate windows too. If -1, all processes will be enabled.

##### Returns

`bool`

`false` if failed.

#### Remarks

In some cases you may need this function because Windows often disables API `SetForegroundWindow` to not allow background applications to activate windows while the user is working (using keyboard/mouse) with the currently active window. Then `SetForegroundWindow` usually just makes the window's taskbar button flash. Usually you don't call `SetForegroundWindow` directly. It is called by some other functions. Don't need to call this function before calling `Au.wnd.Activate` and other functions of this library that activate windows.