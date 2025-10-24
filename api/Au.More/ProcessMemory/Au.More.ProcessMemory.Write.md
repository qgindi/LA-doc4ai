# Method `Au.More.ProcessMemory.Write`

## Overload 1

Copies memory from this process to that process (memory address `Au.More.ProcessMemory.Mem`).

```
public bool Write(void* ptrFrom, int nBytes, int offsetBytes = 0)
```

##### Parameters

- *ptrFrom*  (`void*`):
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

Copies memory from this process to a known address in that process.

```
public bool Write(nint ptrTo, void* ptrFrom, int nBytes)
```

##### Parameters

- *ptrTo*  (`nint`):
    Address of memory in that process.
- *ptrFrom*  (`void*`):
    Address of memory in this process.
- *nBytes*  (`int`):
    Number of bytes to copy.

##### Returns

`bool`

`false` if failed.