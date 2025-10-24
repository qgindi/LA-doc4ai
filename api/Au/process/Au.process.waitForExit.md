# Method `Au.process.waitForExit`

Waits until the process ends.

```
public static bool waitForExit(Seconds timeout, int processId, out int exitCode)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *processId*  (`int`):
    Process id. If invalid but not 0, the function returns `true` and sets `exitCode = int.MinValue`; probably the process is already ended.
- *exitCode*  (`int`):
    Receives the exit code.

##### Returns

`bool`

`true` when the process ended. On timeout returns `false` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).
- `Au.Types.AuException`:
    Failed.
- `ArgumentException`:
    *processId* is 0.