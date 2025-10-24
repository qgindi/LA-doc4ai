# Method `Au.filesystem.moveTo`

Moves file or directory into another directory.

```
public static void moveTo(string path, string newDirectory, FIfExists ifExists = FIfExists.Fail)
```

##### Parameters

- *path*  (`string`):
    Full path.
- *newDirectory*  (`string`):
    Full path of the new parent directory.
- *ifExists*  (`Au.Types.FIfExists`)

##### Exceptions

- `ArgumentException`:

    - *path* or *newDirectory* is not full path (see `Au.pathname.isFullPath`).
    - *path* is drive. To move drive content, use `Au.filesystem.move`.
- `FileNotFoundException`:
    *path* not found.
- `Au.Types.AuException`:
    Failed.

#### Remarks

In most cases uses API `MoveFileEx`. It's fast, because don't need to copy files. In these cases copies/deletes: destination is on another drive; need to merge directories. When need to copy, does not copy security properties; sets default. Creates the destination directory if does not exist (see `Au.filesystem.createDirectory`).