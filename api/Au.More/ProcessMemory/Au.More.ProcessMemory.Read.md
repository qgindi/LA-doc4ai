# Method `Au.More.ProcessMemory.Read`

## Overload 1

Copies memory from that process (memory address `Au.More.ProcessMemory.Mem`) to this process.

```
public bool Read(void* ptrTo, int nBytes, int offsetBytes = 0)
```

##### Parameters

- *ptrTo*  (`void*`):
    Address of memory in this process.
- *nBytes*  (`int`):
    Number of bytes to copy.
- *offsetBytes*  (`int`):
    Offset in `Au.More.ProcessMemory.Mem`.

##### Returns

`bool`

`false` if failed.

* * *

## Overload 2

Copies memory from a known address in that process to this process.

```
public bool Read(nint ptrFrom, void* ptrTo, int nBytes)
```

##### Parameters

- *ptrFrom*  (`nint`):
    Address of memory in that process.
- *ptrTo*  (`void*`):
    Address of memory in this process.
- *nBytes*  (`int`):
    Number of bytes to copy.

##### Returns

`bool`

`false` if failed.