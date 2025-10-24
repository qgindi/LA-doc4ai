# Method `Au.wait.doEventsUntil`

Waits for a condition to be changed while processing messages or other events received by this thread.

```
public static bool doEventsUntil(Seconds timeout, Func<bool> condition)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *condition*  (`Func<bool>`):
    Callback function that returns `true` to stop waiting. More info in Remarks.

##### Returns

`bool`

Returns `true`. On timeout returns `false` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).

#### Remarks

While waiting, dispatches Windows messages etc, like `Au.wait.doEvents`. After dispatching one or more messages or other events (posted messages, messages sent by other threads, hooks, COM, APC, etc), calls the callback function. Stops waiting when it returns `true`. Similar to `Au.wait.until<T>`. Differences: 1. Always dispatches messages etc. 2. Does not call the callback function when there are no messages etc. 3. Does not use `Au.More.WaitLoop`, `Au.Types.Seconds.Period`, `Au.Types.Seconds.MaxPeriod` and `Au.Types.Seconds.DoEvents`.

#### Examples

```
bool stop = false;
timer.after(2000, t => { print.it("timer"); stop = true; });
wait.doEventsUntil(5, () => stop);
print.it(stop);
```