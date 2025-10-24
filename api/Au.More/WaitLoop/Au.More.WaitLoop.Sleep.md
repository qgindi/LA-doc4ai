# Method `Au.More.WaitLoop.Sleep`

Calls `Au.More.WaitLoop.IsTimeout`. If it returns `true`, returns `false`. Else sleeps `Au.More.WaitLoop.Period` milliseconds, increments `Period` if it is less than `Au.More.WaitLoop.MaxPeriod`, and returns `true`.

```
public bool Sleep()
```

##### Returns

`bool`

##### Exceptions

- `TimeoutException`:
    The timeout time has expired (if > 0).