# Property `Au.wnd.IsOfThisProcess`

Returns `true` if this window belongs to the current process, `false` if to another process. Also returns `false` when fails (probably window closed or 0 handle). Supports `Au.lastError`. Calls API `GetWindowThreadProcessId`.

```
public bool IsOfThisProcess { get; }
```

##### Property Value

`bool`