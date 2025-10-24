# Property `Au.wnd.IsOfThisThread`

Returns `true` if this window belongs to the current thread, `false` if to another thread. Also returns `false` when fails (probably window closed or 0 handle). Supports `Au.lastError`. Calls API `GetWindowThreadProcessId`.

```
public bool IsOfThisThread { get; }
```

##### Property Value

`bool`