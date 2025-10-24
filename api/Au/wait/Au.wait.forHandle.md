# Method `Au.wait.forHandle`

Waits for a kernel object (event, mutex, etc).

```
public static int forHandle(Seconds timeout, WHFlags flags, params ReadOnlySpan<nint> handles)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *flags*  (`Au.Types.WHFlags`)
- *handles*  (`ReadOnlySpan<nint>`):
    One or more handles of kernel objects. Max 63.

##### Returns

`int`

Returns 1-based index of the first signaled handle. Negative if abandoned mutex. On timeout returns 0 if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).
- `Au.Types.AuException`:
    Failed. For example a handle is invalid.

#### Remarks

Uses API `WaitForMultipleObjectsEx` or `MsgWaitForMultipleObjectsEx`. Alertable. Does not use `Au.More.WaitLoop`, `Au.Types.Seconds.Period` and `Au.Types.Seconds.MaxPeriod`.