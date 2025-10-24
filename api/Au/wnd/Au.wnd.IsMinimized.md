# Property `Au.wnd.IsMinimized`

Returns `true` if minimized, `false` if not. Also returns `false` when fails (probably window closed or 0 handle). Supports `Au.lastError`. Calls API `IsIconic`.

```
public bool IsMinimized { get; }
```

##### Property Value

`bool`