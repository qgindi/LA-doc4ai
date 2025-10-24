# Method `Au.More.MemoryUtil.FreeAlloc`

Frees a memory block (if not `null`) and allocates new.

```
public static void FreeAlloc<T>(ref T* mem, nint count, bool zeroInit = false) where T : unmanaged
```

##### Parameters

- *mem*  (`T*`):
    Input: old memory address or `null`. Output: new memory address; `null` if exception (it prevents freeing twice).
- *count*  (`nint`):
    New count of elements of type `T`.
- *zeroInit*  (`bool`):
    Set all bytes = 0.

##### Exceptions

- `OutOfMemoryException`:
    Failed. Probably *count* is too big.

##### Type Parameters

- `T`

#### Remarks

At first sets *mem* = `null`, to avoid double `Au.More.MemoryUtil.Free` if this function throws exception. Then calls `Au.More.MemoryUtil.Free` and `Au.More.MemoryUtil.Alloc`.