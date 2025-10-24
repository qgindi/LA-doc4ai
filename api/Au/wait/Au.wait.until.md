# Method `Au.wait.until`

Waits for a user-defined condition. Until the callback function returns a value other than `default(T)`, for example `true`.

```
public static T until<T>(Seconds timeout, Func<T> condition)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *condition*  (`Func<T>`):
    Callback function (eg lambda). It is called repeatedly, until returns a value other than `default(T)`. Default period is 10, and can be changed like `wait.until(new(5) { Timeout = 100 }, ...)`.

##### Returns

`T`

Returns the value returned by the callback function. On timeout returns `default(T)` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`

##### Type Parameters

- `T`

#### Examples

See `Au.wait`.