# Method `Au.More.MemoryUtil.ReAlloc`

Reallocates a memory block to make it bigger or smaller.

```
public static void ReAlloc<T>(ref T* mem, nint count, bool zeroInit = false) where T : unmanaged
```

##### Parameters

- *mem*  (`T*`):
    Input: old memory address; if `null`, allocates new memory like `Au.More.MemoryUtil.Alloc<T>`. Output: new memory address. Unchanged if exception.
- *count*  (`nint`):
    New count of elements of type `T`.
- *zeroInit*  (`bool`):
    When size is growing, set all added bytes = 0.

##### Exceptions

- `OutOfMemoryException`:
    Failed. Probably *count* is too big.

##### Type Parameters

- `T`

#### Remarks

Calls API `HeapReAlloc` or `HeapAlloc`. Preserves data in `Math.Min(oldCount, newCount)` elements of old memory (copies from old memory if need). The memory is unmanaged and will not be freed automatically. Always call `Au.More.MemoryUtil.Free` when done. Call `ReAlloc` or `Au.More.MemoryUtil.FreeAlloc<T>` if need to resize.