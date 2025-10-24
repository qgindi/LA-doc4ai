# Method `Au.process.processIdFromHandle`

Gets process id from handle (API `GetProcessId`).

```
public static int processIdFromHandle(nint processHandle)
```

##### Parameters

- *processHandle*  (`nint`):
    Process handle.

##### Returns

`int`

0 if failed. Supports `Au.lastError`.