# Method `Au.filesystem.more.calculateDirectorySize`

Calls `Au.filesystem.enumerate` and returns the sum of all descendant file sizes. With default flags, it includes sizes of all descendant files, in this directory and all subdirectories except in inaccessible [sub]directories.

```
public static long calculateDirectorySize(string path, FEFlags flags = FEFlags.AllDescendants | FEFlags.IgnoreInaccessible)
```

##### Parameters

- *path*  (`string`):
    Full path.
- *flags*  (`Au.Types.FEFlags`):
    `Au.filesystem.enumerate` flags.

##### Returns

`long`

##### Exceptions

- `Exception`:
    Exceptions of `Au.filesystem.enumerate`. By default no exceptions if used full path and the directory exists.

#### Remarks

This function is slow if the directory is large. Don't use this function for files (throws exception) and drives (instead use `System.IO.DriveInfo`, it's fast and includes sizes of Recycle Bin and other protected hidden system directories).