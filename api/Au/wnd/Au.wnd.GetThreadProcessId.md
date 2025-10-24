# Method `Au.wnd.GetThreadProcessId`

Gets native thread id and process id of this window. Calls API `GetWindowThreadProcessId`.

```
public int GetThreadProcessId(out int processId)
```

##### Parameters

- *processId*  (`int`)

##### Returns

`int`

Thread id, or 0 if failed. Supports `Au.lastError`.

#### Remarks

It is not the same as `System.Environment.CurrentManagedThreadId`.