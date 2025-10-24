# Property `Au.More.WaitLoop.MaxPeriod`

Maximal period (`Au.More.WaitLoop.Sleep` sleep time). Milliseconds. Initially it is `Au.Types.Seconds.MaxPeriod`, or `Au.More.WaitLoop.Period` `*` 50 if it is `null` (eg `10*50=500`).

```
public float MaxPeriod { readonly get; set; }
```

##### Property Value

`float`