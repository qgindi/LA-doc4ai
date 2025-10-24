# Method `Au.filesystem.move`

Moves (changes path of) file or directory.

```
public static void move(string path, string newPath, FIfExists ifExists = FIfExists.Fail)
```

##### Parameters

- *path*  (`string`):
    Full path.
- *newPath*  (`string`):

    New full path.

    > **Note:**
    >     It is not the new parent directory. See `Au.filesystem.moveTo`.
- *ifExists*  (`Au.Types.FIfExists`)

##### Exceptions

- `ArgumentException`:
    *path* or *newPath* is not full path (see `Au.pathname.isFullPath`).
- `FileNotFoundException`:
    *path* not found.
- `Au.Types.AuException`:
    Failed.

#### Remarks

In most cases uses API `MoveFileEx`. It's fast, because don't need to copy files. In these cases copies/deletes: destination is on another drive; need to merge directories. When need to copy, does not copy security properties; sets default. Creates the destination directory if does not exist (see `Au.filesystem.createDirectory`). If *path* and *newPath* share the same parent directory, just renames the file.