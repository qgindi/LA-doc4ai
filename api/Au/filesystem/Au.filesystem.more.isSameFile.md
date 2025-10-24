# Method `Au.filesystem.more.isSameFile`

Returns `true` if two paths are of the same existing file, regardless of path format etc.

```
public static bool isSameFile(string path1, string path2, bool useSymlink = false)
```

##### Parameters

- *path1*  (`string`):
    Path of a file or directory. Supports environment variables (see `Au.pathname.expand`) and paths relative to current directory.
- *path2*  (`string`):
    Path of a file or directory. Supports environment variables (see `Au.pathname.expand`) and paths relative to current directory.
- *useSymlink*  (`bool`):
    If a path is of a symbolic link, use the link. If `false`, uses its target; for example, returns `false` if the target doesn't exist.

##### Returns

`bool`

##### Exceptions

- `ArgumentException`:
    Not full path.

### See Also

`Au.filesystem.more.comparePaths`