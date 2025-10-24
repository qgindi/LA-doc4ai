# Property `Au.uacInfo.IntegrityLevel`

Gets the [UAC](../articles/UAC.html) integrity level (IL) of the process.

```
public UacIL IntegrityLevel { get; }
```

##### Property Value

`Au.Types.UacIL`

#### Remarks

IL from lowest to highest value: `Untrusted`, `Low`, `Medium`, `UIAccess`, `High`, `System`, `Protected`, `Unknown`. The IL enum member values can be used like `if(x.IntegrityLevel > IL.Medium) ...` . If UAC is turned off, most non-service processes on administrator account have High IL; on non-administrator - Medium.