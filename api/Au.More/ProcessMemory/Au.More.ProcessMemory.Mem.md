# Property `Au.More.ProcessMemory.Mem`

Address in that process used by the read and write functions.

```
public nint Mem { get; set; }
```

##### Property Value

`nint`

#### Remarks

Most read/write functions of this class don't have a parameter "address in that process". Instead they use `Mem`, which initially is == `Au.More.ProcessMemory.MemAllocated`. But you can set `Mem` = any valid address in that process; usually you do it when no memory is allocated by the constructor (*nBytes* 0). The address is invalid in this process.