# Method `Au.wnd.WaitForName`

Waits until this window has the specified name.

```
public bool WaitForName(Seconds timeout, string name, bool not = false)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *name*  (`string`):
    Window name. Usually it is the title bar text. String format: [wildcard expression](../articles/Wildcard%20expression.html).
- *not*  (`bool`):
    Wait until this window does not have the specified name.

##### Returns

`bool`

Returns `true`. On timeout returns `false` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).
- `Au.Types.AuWndException`:
    The window handle is invalid or the window was closed while waiting.
- `ArgumentException`:
    Invalid wildcard expression.