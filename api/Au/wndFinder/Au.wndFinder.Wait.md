# Method `Au.wndFinder.Wait`

Waits until window exists or is active.

```
public wnd Wait(Seconds timeout, bool active)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *active*  (`bool`):
    The window must be the active window (`Au.wnd.active`), and not minimized.

##### Returns

`Au.wnd`

Returns `Au.wndFinder.Result`. On timeout returns `default(wnd)` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).

#### Remarks

Same as `Au.wndFinder.Find`, except:

- 0 timeout means infinite.
- on timeout throws `System.TimeoutException`, not `Au.Types.NotFoundException`.
- has parameter *active*.