# Property `Au.wnd.ThreadId`

Gets native thread id of this window. Calls API `GetWindowThreadProcessId`.

```
public int ThreadId { get; }
```

##### Property Value

`int`

0 if failed. Supports `Au.lastError`.

#### Remarks

It is not the same as `System.Environment.CurrentManagedThreadId`.