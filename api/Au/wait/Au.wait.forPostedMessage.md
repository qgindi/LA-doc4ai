# Method `Au.wait.forPostedMessage`

Waits for a posted message received by this thread.

```
public static bool forPostedMessage(Seconds timeout, WPMCallback callback)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *callback*  (`Au.Types.WPMCallback`):
    Callback function that returns `true` to stop waiting. More info in Remarks.

##### Returns

`bool`

Returns `true`. On timeout returns `false` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).

#### Remarks

While waiting, dispatches Windows messages etc, like `Au.wait.doEvents`. Before dispatching a posted message, calls the callback function. Stops waiting when it returns `true`. Does not dispatch the message if the function sets the message field = 0. Does not use `Au.More.WaitLoop`, `Au.Types.Seconds.Period`, `Au.Types.Seconds.MaxPeriod` and `Au.Types.Seconds.DoEvents`.

#### Examples

```
timer.after(2000, t => { print.it("timer"); });
wait.forPostedMessage(5, (ref MSG m) => { print.it(m); return m.message == 0x113; }); //WM_TIMER
print.it("finished");
```