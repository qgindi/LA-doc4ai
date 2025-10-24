# Property `Au.wnd.IsMaximized`

Returns `true` if maximized, `false` if not. Also returns `false` when fails (probably window closed or 0 handle). Supports `Au.lastError`. Calls API `IsZoomed`.

```
public bool IsMaximized { get; }
```

##### Property Value

`bool`