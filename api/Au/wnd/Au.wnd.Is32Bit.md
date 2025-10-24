# Property `Au.wnd.Is32Bit`

Returns `true` if the window is of a 32-bit process, `false` if of a 64-bit process. Also returns `false` if failed. Supports `Au.lastError`.

```
public bool Is32Bit { get; }
```

##### Property Value

`bool`

#### Remarks

> **Note:**
> If you know that the window belongs to current process, instead use `Au.osVersion` functions or `IntPtr.Size==4`. This function is much slower.