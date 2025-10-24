# Method `Au.More.MemoryUtil.VirtualAlloc`

Allocates new virtual memory block with API `VirtualAlloc` and returns its address: `VirtualAlloc(default, size, MEM_COMMIT|MEM_RESERVE, PAGE_READWRITE)`.

```
public static byte* VirtualAlloc(nint size)
```

##### Parameters

- *size*  (`nint`):
    Byte count.

##### Returns

`byte*`

##### Exceptions

- `OutOfMemoryException`:
    Failed. Probably *size* is too big.

#### Remarks

Faster than managed and `Au.More.MemoryUtil.Alloc` when memory size is large, more than 1 MB; else slower. The memory is initialized to zero (all bytes 0).