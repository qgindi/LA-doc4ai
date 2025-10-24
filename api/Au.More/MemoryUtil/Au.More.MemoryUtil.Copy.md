# Method `Au.More.MemoryUtil.Copy`

Copies memory with `System.Buffer.MemoryCopy`.

```
public static void Copy(void* from, void* to, nint size)
```

##### Parameters

- *from*  (`void*`)
- *to*  (`void*`)
- *size*  (`nint`)

#### Remarks

If some part of memory blocks overlaps, this function is much slower than `Au.More.MemoryUtil.Move`. Else same speed or slightly faster.