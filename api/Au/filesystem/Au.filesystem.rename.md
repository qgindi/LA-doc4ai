# Method `Au.filesystem.rename`

Renames file or directory.

```
public static void rename(string path, string newName, FIfExists ifExists = FIfExists.Fail)
```

##### Parameters

- *path*  (`string`):
    Full path.
- *newName*  (`string`):
    New name without path. Example: `"name.txt"`.
- *ifExists*  (`Au.Types.FIfExists`)

##### Exceptions

- `ArgumentException`:

    - *path* is not full path (see `Au.pathname.isFullPath`).
    - *newName* is invalid filename.
- `FileNotFoundException`:
    *path* not found.
- `Au.Types.AuException`:
    Failed.

#### Remarks

Uses API `MoveFileEx`.