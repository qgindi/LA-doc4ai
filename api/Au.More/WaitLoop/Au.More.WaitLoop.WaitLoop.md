# Constructor of `Au.More.WaitLoop`

Sets timeout and possibly more wait parameters.

```
public WaitLoop(Seconds timeout)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout in seconds, like `3` or `0.5`. Or a `Seconds` variable containing timeout etc, like `new(3, period: 5)`. If timeout is 0, will wait indefinitely. If `>` 0, `Au.More.WaitLoop.Sleep` throws `System.TimeoutException` when timed out. If \< 0, `Sleep` then returns `false` instead.