# Constructor of `Au.Types.Seconds`

Sets timeout. Example: `var w = wnd.find(new Seconds(3) { Period = 5, MaxPeriod = 50 }, "Name");`.

```
public Seconds(double time)
```

##### Parameters

- *time*  (`double`):
    Timeout, in seconds. Negative value means "don't throw exception when timed out". Value 0 means "wait indefinitely" when used with `WaitX` functions; with `FindX` functions it means "don't wait". More info: [Wait timeout](../articles/Wait%20timeout.html).