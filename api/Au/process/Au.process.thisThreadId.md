# Property `Au.process.thisThreadId`

Gets native thread id of this thread (API `GetCurrentThreadId`).

```
public static int thisThreadId { get; }
```

##### Property Value

`int`

#### Remarks

It is not the same as `System.Environment.CurrentManagedThreadId`.

### See Also

`Au.wnd.ThreadId`