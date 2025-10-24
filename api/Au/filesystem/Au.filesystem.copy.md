# Method `Au.filesystem.copy`

Copies file or directory.

```
public static void copy(string path, string newPath, FIfExists ifExists = FIfExists.Fail, FCFlags copyFlags = 0, Func<FEFile, bool> fileFilter = null, Func<FEFile, int> dirFilter = null)
```

##### Parameters

- *path*  (`string`):
    Full path.
- *newPath*  (`string`):

    Full path of the destination.

    > **Note:**
    >     It is not the new parent directory. See `Au.filesystem.copyTo`.
- *ifExists*  (`Au.Types.FIfExists`)
- *copyFlags*  (`Au.Types.FCFlags`):
    Options used when copying directory.
- *fileFilter*  (`Func<Au.Types.FEFile, bool>`):
    Callback function that decides which files to copy when copying directory. See `Au.filesystem.enumerate`. Note: this function uses `Au.Types.FEFlags.NeedRelativePaths`.
- *dirFilter*  (`Func<Au.Types.FEFile, int>`):
    Callback function that decides which subdirectories to copy when copying directory. See `Au.filesystem.enumerate`. Note: this function uses `Au.Types.FEFlags.NeedRelativePaths`.

##### Exceptions

- `ArgumentException`:
    *path* or *newPath* is not full path (see `Au.pathname.isFullPath`).
- `FileNotFoundException`:
    *path* not found.
- `Au.Types.AuException`:
    Failed.

#### Remarks

Uses API `CopyFileEx` and `CreateDirectoryEx`. On Windows 7 does not copy security properties; sets default. Does not copy symbolic links (silently skips, no exception) if this process is not running as administrator. Creates the destination directory if does not exist (see `Au.filesystem.createDirectory`).