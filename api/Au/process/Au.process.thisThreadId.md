# Property `Au.process.thisThreadId`

Gets native thread id of this thread (API `GetCurrentThreadId`).

```csharp
public static int thisThreadId { get; }
```

##### Property Value

`int`

#### Remarks

It is not the same as `System.Environment.CurrentManagedThreadId`.

### See Also

`Au.wnd.ThreadId`