# Method `Au.wnd.NameIs`

If window name matches one of strings in *names*, returns 1-based string index. Else returns 0. Also returns 0 if fails to get name (probably window closed or 0 handle). Supports `Au.lastError`.

```
public int NameIs(params ReadOnlySpan<string> names)
```

##### Parameters

- *names*  (`ReadOnlySpan<string>`):
    Window names. Case-insensitive wildcard. See `Au.Types.ExtString.Like`. The array and strings cannot be `null`.

##### Returns

`int`