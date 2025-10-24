# Method `Au.More.MemoryUtil.Move`

Copies memory with API `memmove`.

```
public static void Move(void* from, void* to, nint size)
```

##### Parameters

- *from*  (`void*`)
- *to*  (`void*`)
- *size*  (`nint`)

#### Remarks

If some part of memory blocks overlaps, this function is much faster than `Au.More.MemoryUtil.Copy`. Else same speed or slightly slower.