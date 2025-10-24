# Property `Au.wnd.IsUnicode`

Returns `true` if the window is a Unicode window, `false` if ANSI. Also returns `false` when fails (probably window closed or 0 handle). Supports `Au.lastError`. Calls API `IsWindowUnicode`.

```
public bool IsUnicode { get; }
```

##### Property Value

`bool`