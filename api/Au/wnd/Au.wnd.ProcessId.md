# Property `Au.wnd.ProcessId`

Gets native process id of this window. Calls API `GetWindowThreadProcessId`.

```
public int ProcessId { get; }
```

##### Property Value

`int`

0 if failed. Supports `Au.lastError`.