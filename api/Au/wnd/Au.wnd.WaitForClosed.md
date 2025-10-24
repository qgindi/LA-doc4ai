# Method `Au.wnd.WaitForClosed`

Waits until this window is closed/destroyed or until its process ends.

```
public bool WaitForClosed(Seconds timeout, bool waitUntilProcessEnds = false)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *waitUntilProcessEnds*  (`bool`):
    Wait until the process of this window ends.

##### Returns

`bool`

Returns `true`. On timeout returns `false` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).
- `Au.Types.AuException`:
    Failed to open process handle when *waitUntilProcessEnds* is `true`.

#### Remarks

If the window is already closed, immediately returns `true`.