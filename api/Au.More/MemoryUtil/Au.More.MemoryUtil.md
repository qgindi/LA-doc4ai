# Class `Au.More.MemoryUtil`

Allocates memory from native heap of this process using heap API. Also has more functions to work with memory: copy, move, virtual alloc.

```
public static class MemoryUtil
```

##### Remarks

Uses the common heap of this process, API `GetProcessHeap`.

##### Inheritance

`object` → `MemoryUtil`

### Methods

`Alloc`, `Alloc<T>`, `Copy`, `Free`, `FreeAlloc<T>`, `Move`, `ReAlloc<T>`, `VirtualAlloc`, `VirtualFree`