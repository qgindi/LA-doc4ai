# Method `Au.wait.retry`

## Overload 1

Calls callback function *action*. If it throws an exception, waits/retries until it does not throw exceptions or until timeout.

```
public static bool retry(Seconds timeout, Action action, Func<Exception, bool> catchWhen = null)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *action*  (`Action`):
    Callback function (eg lambda). It is called repeatedly, until does not throw an exception. Default period is 10, and can be changed like `wait.retry(new(5) { Timeout = 100 }, ...)`.
- *catchWhen*  (`Func<Exception, bool>`):
    Called on exception. Return `true` to handle the exception (and wait/retry). Return `false` to not handle the exception. If `null` (default), handles all exceptions.

##### Returns

`bool`

Returns `true` when *action* succeeded. On timeout returns `false` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`

#### Examples

This example uses both `wait.retry` overloads - with parameter `Func func` and with parameter `Action action`.

```
string file = @"C:\Test\test.txt";
string s = wait.retry(5, () => File.ReadAllText(file));
s = s.Upper();
wait.retry(5, () => { File.WriteAllText(file, s); });
print.it("ok");
```

Set the retry period.

```
wait.retry(new(5) { Period = 100, MaxPeriod = 1000 }, () => { File.WriteAllText(file, s); });
```

Handle only exceptions of some types.

```
wait.retry(5, () => { File.WriteAllText(file, s); }, e => e is IOException);
```

* * *

## Overload 2

Calls callback function *func* and returns its result. If it throws an exception, waits/retries until it does not throw exceptions or until timeout.

```
public static T retry<T>(Seconds timeout, Func<T> func, Func<Exception, bool> catchWhen = null)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *func*  (`Func<T>`):
    Callback function (eg lambda). It is called repeatedly, until does not throw an exception. Default period is 10, and can be changed like `wait.retry(new(5) { Timeout = 100 }, ...)`.
- *catchWhen*  (`Func<Exception, bool>`):
    Called on exception. Return `true` to handle the exception (and wait/retry). Return `false` to not handle the exception. If `null` (default), handles all exceptions.

##### Returns

`T`

Returns the value returned by the callback function. On timeout returns `default(T)` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`

##### Type Parameters

- `T`