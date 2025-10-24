# Method `Au.More.MemoryUtil.Alloc`

## Overload 1

Allocates new memory block and returns its address.

```
public static byte* Alloc(nint size, bool zeroInit = false)
```

##### Parameters

- *size*  (`nint`):
    Byte count.
- *zeroInit*  (`bool`):
    Set all bytes = 0.

##### Returns

`byte*`

##### Exceptions

- `OutOfMemoryException`:
    Failed. Probably *size* is too big.

#### Remarks

Calls API `HeapAlloc`. The memory is unmanaged and will not be freed automatically. Always call `Au.More.MemoryUtil.Free` when done. Call `Au.More.MemoryUtil.ReAlloc<T>` or `Au.More.MemoryUtil.FreeAlloc<T>` if need to resize.

* * *

## Overload 2

Allocates new memory block and returns its address.

```
public static T* Alloc<T>(nint count, bool zeroInit = false) where T : unmanaged
```

##### Parameters

- *count*  (`nint`):
    Count of elements of type `T`.
- *zeroInit*  (`bool`):
    Set all bytes = 0.

##### Returns

`T*`

##### Exceptions

- `OutOfMemoryException`:
    Failed. Probably *size* is too big.

##### Type Parameters

- `T`

#### Remarks

Calls API `HeapAlloc`. The memory is unmanaged and will not be freed automatically. Always call `Au.More.MemoryUtil.Free` when done. Call `Au.More.MemoryUtil.ReAlloc<T>` or `Au.More.MemoryUtil.FreeAlloc<T>` if need to resize.