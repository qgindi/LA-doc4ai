# Method `Au.elm.WaitFor`

Waits for a user-defined state/condition of this UI element. For example enabled, checked, changed name.

```
public T WaitFor<T>(Seconds timeout, Func<elm, T> condition)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *condition*  (`Func<Au.elm, T>`):
    Callback function (eg lambda). It is called repeatedly, until returns a value other than `default(T)`, for example `true`.

##### Returns

`T`

Returns the value returned by the callback function. On timeout returns `default(T)` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).
- `Au.Types.AuWndException`:
    Failed to get container window (`Au.elm.WndContainer`), or it was closed while waiting.

##### Type Parameters

- `T`