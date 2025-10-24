# Property `Au.More.ProcessMemory.MemAllocated`

Address of memory allocated in that process.

```
public nint MemAllocated { get; set; }
```

##### Property Value

`nint`

#### Remarks

The constructor allocates memory with API `VirtualAllocEx` if *nBytes* != 0. Finally `Dispose` will free it with API `VirtualFreeEx`. The setter normally isn't used; if you set `MemAllocated = default`, `Dispose` will not free the memory. The address is invalid in this process.