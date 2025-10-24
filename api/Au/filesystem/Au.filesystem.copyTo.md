# Method `Au.filesystem.copyTo`

Copies file or directory into another directory.

```
public static void copyTo(string path, string newDirectory, FIfExists ifExists = FIfExists.Fail, FCFlags copyFlags = 0, Func<FEFile, bool> fileFilter = null, Func<FEFile, int> dirFilter = null)
```

##### Parameters

- *path*  (`string`):
    Full path.
- *newDirectory*  (`string`):
    Full path of the new parent directory.
- *ifExists*  (`Au.Types.FIfExists`)
- *copyFlags*  (`Au.Types.FCFlags`):
    Options used when copying directory.
- *fileFilter*  (`Func<Au.Types.FEFile, bool>`):
    Callback function that decides which files to copy when copying directory. See `Au.filesystem.enumerate`. Note: this function uses `Au.Types.FEFlags.NeedRelativePaths`.
- *dirFilter*  (`Func<Au.Types.FEFile, int>`):
    Callback function that decides which subdirectories to copy when copying directory. See `Au.filesystem.enumerate`. Note: this function uses `Au.Types.FEFlags.NeedRelativePaths`.

##### Exceptions

- `ArgumentException`:

    - *path* or *newDirectory* is not full path (see `Au.pathname.isFullPath`).
    - *path* is drive. To copy drive content, use `Au.filesystem.copy`.
- `FileNotFoundException`:
    *path* not found.
- `Au.Types.AuException`:
    Failed.

#### Remarks

Uses API `CopyFileEx` and `CreateDirectoryEx`. On Windows 7 does not copy security properties; sets default. Does not copy symbolic links (silently skips, no exception) if this process is not running as administrator. Creates the destination directory if does not exist (see `Au.filesystem.createDirectory`).