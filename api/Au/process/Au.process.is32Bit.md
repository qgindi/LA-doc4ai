# Method `Au.process.is32Bit`

## Overload 1

Returns `true` if the process is 32-bit, `false` if 64-bit. Also returns `false` if failed. Supports `Au.lastError`.

```
public static bool is32Bit(int processId)
```

##### Parameters

- *processId*  (`int`)

##### Returns

`bool`

#### Remarks

> **Note:**
> If you know it is current process, instead use `Au.osVersion` functions or `IntPtr.Size==4`. This function is much slower.

### See Also

`System.Runtime.InteropServices.RuntimeInformation`

* * *

## Overload 2

Returns `true` if the process is 32-bit, `false` if 64-bit. Also returns `false` if failed. Supports `Au.lastError`.

```
public static bool is32Bit(nint processHandle)
```

##### Parameters

- *processHandle*  (`nint`)

##### Returns

`bool`