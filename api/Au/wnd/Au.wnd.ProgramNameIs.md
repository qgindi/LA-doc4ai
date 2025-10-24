# Method `Au.wnd.ProgramNameIs`

If window program name matches one of strings in *programNames*, returns 1-based string index. Else returns 0. Also returns 0 if fails to get program name (probably window closed or 0 handle). Supports `Au.lastError`.

```
public int ProgramNameIs(params ReadOnlySpan<string> programNames)
```

##### Parameters

- *programNames*  (`ReadOnlySpan<string>`):
    Program names, like `"notepad.exe"`. Case-insensitive wildcard. See `Au.Types.ExtString.Like`. The array and strings cannot be `null`.

##### Returns

`int`