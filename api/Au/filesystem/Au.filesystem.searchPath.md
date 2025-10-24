# Method `Au.filesystem.searchPath`

Finds file or directory and returns full path.

```
public static string searchPath(string path, params string[] dirs)
```

##### Parameters

- *path*  (`string`):
    Full or relative path or just filename with extension. Supports network paths too.
- *dirs*  (`string[]`):
    0 or more directories where to search.

##### Returns

`string`

`null` if not found.

#### Remarks

If the *path* argument is full path, calls `Au.filesystem.exists` and returns normalized path if exists, `null` if not. Else searches in these places:

1. *dirs*, if used.
2. `Au.folders.ThisApp`.
3. Calls API `SearchPath`, which searches in the process directory, Windows system directories, current directory, `PATH` environment variable. The search order depends on API `SetSearchPathMode` or registry settings.
4. If *path* ends with `".exe"`, tries to get path from registry "App Paths" keys.