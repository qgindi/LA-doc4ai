# Property `Au.More.WaitLoop.Period`

Current period (`Au.More.WaitLoop.Sleep` sleep time). Milliseconds. Initially it is `Au.Types.Seconds.Period`, or 10 ms if it was `null`. Then each `Au.More.WaitLoop.Sleep` increments it until `Au.More.WaitLoop.MaxPeriod`.

```
public float Period { readonly get; set; }
```

##### Property Value

`float`