# Method `Au.pathname.makeUnique`

Creates path with unique filename for a new file or directory. If the specified path is of an existing file or directory, returns path where the filename part is modified like `"file 2.txt"`, `"file 3.txt"` etc. Else returns unchanged *path*.

```
public static string makeUnique(string path, bool isDirectory)
```

##### Parameters

- *path*  (`string`):
    Suggested full path.
- *isDirectory*  (`bool`):
    The path is for a directory. The number is always appended at the very end, not before `.extension`.

##### Returns

`string`