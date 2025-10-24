# Method `Au.More.MemoryUtil.Free`

Frees a memory block. Does nothing if *mem* is `null`.

```
public static void Free(void* mem)
```

##### Parameters

- *mem*  (`void*`)

#### Remarks

Calls API `HeapFree`.