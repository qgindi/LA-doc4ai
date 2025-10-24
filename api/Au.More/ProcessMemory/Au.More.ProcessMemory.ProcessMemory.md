# Constructor of `Au.More.ProcessMemory`

## Overload 1

Opens process handle and optionally allocates memory in that process.

```
public ProcessMemory(int processId, int nBytes, bool noException = false)
```

##### Parameters

- *processId*  (`int`):
    Process id.
- *nBytes*  (`int`):
    If not 0, allocates memory of this size in that process.
- *noException*  (`bool`):
    Don't throw exceptions. If failed, sets `Au.More.ProcessMemory.ProcessHandle` = default.

##### Exceptions

- `Au.Types.AuException`:
    Failed to open process handle (usually because of [UAC](../articles/UAC.html)) or allocate memory.

* * *

## Overload 2

Opens process handle and optionally allocates memory in that process.

```
public ProcessMemory(wnd w, int nBytes, bool noException = false)
```

##### Parameters

- *w*  (`Au.wnd`):
    A window of that process.
- *nBytes*  (`int`):
    If not 0, allocates memory of this size in that process.
- *noException*  (`bool`):
    Don't throw exceptions. If failed, sets `Au.More.ProcessMemory.ProcessHandle` = default.

##### Exceptions

- `Au.Types.AuWndException`:
    *w* invalid.
- `Au.Types.AuException`:
    Failed to open process handle or allocate memory.