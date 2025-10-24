# Method `Au.pathname.isFullPath`

Returns `true` if the string is full path, like `@"C:\a\b.txt"` or `@"C:"` or `@"\\server\share\..."`:

```
public static bool isFullPath(ReadOnlySpan<char> path, bool orEnvVar = false)
```

##### Parameters

- *path*  (`ReadOnlySpan<char>`):
    Any string. Can be `null`.
- *orEnvVar*  (`bool`):
    Also return `true` if starts with `"%environmentVariable%"` or `"%folders.Folder%"`. Note: this function does not check whether the variable/folder exists; for it use `Au.pathname.isFullPathExpand` instead.

##### Returns

`bool`

#### Remarks

Returns `true` if *path* matches one of these wildcard patterns:

- `@"?:\*"` - local path, like `@"C:\a\b.txt"`. Here `?` is A-Z, a-z.
- `@"?:"` - drive name, like `@"C:"`. Here `?` is A-Z, a-z.
- `@"\\*"` - network path, like `@"\\server\share\..."`. Or has prefix `@"\\?\"`.

Supports `'/'` characters too.

Supports only file-system paths. Returns `false` if *path* is URL (`Au.pathname.isUrl`) or starts with `"::"`.