# Property `Au.Types.Seconds.Time`

Timeout, in seconds.
Negative value means "don't throw exception when timed out".
Value 0 means "wait indefinitely" when used with`WaitX` functions; with `FindX`functions it means "don't wait".
More info:[Wait timeout](🔗).

```csharp
public double Time { get; set; }
```

##### Property Value

`double`