# Property `Au.More.CpuUsage.ProcessorCount`

Get the number of logical CPU in the system.

```
public static int ProcessorCount { get; }
```

##### Property Value

`int`

#### Remarks

Unlike `System.Environment.ProcessorCount`, does not depend on process affinity etc.