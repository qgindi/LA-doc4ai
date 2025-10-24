# Property `Au.Types.Seconds.Period`

The sleep time between checking the wait condition periodically. Milliseconds. If `null`, will be used a value that usually is best for that wait function, in most cases 10.

```
public int? Period { get; set; }
```

##### Property Value

`int?`

#### Remarks

Most wait functions of this library use `Au.More.WaitLoop`, which repeatedly checks the wait condition and sleeps (waits) several ms. This property sets the initial sleep time (`Au.More.WaitLoop.Period`), which then is incremented by `Period/10` ms in each loop until reaches `Au.More.WaitLoop.MaxPeriod`, which is `Period*50` by default. This property makes the response time shorter or longer. If less than the default value, makes it shorter (faster response), but increases CPU usage; if greater, makes it longer (slower response).