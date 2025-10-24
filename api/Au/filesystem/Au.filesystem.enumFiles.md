# Method `Au.filesystem.enumFiles`

Gets names and other info of matching files in the specified directory.

```
public static IEnumerable<FEFile> enumFiles(string directoryPath, string pattern = null, FEFlags flags = 0)
```

##### Parameters

- *directoryPath*  (`string`):
    Full path of the directory.
- *pattern*  (`string`):

    File name pattern. Format: [wildcard expression](../articles/Wildcard%20expression.html). Used only for files, not for subdirectories. Can be `null`. Examples:

    - `"*.png"` (only png files),
    - `"**m *.png||*.bmp"` (only png and bmp files),
    - `"**nm *.png||*.bmp"` (all files except png and bmp),
    - `@"**r \.html?$"` (regular expression that matches `.htm` and `.html` files).
- *flags*  (`Au.Types.FEFlags`):
    Flags. The function also adds flag `OnlyFiles`.

##### Returns

`IEnumerable<Au.Types.FEFile>`

An enumerable collection of `Au.Types.FEFile` objects.

##### Exceptions

- `ArgumentException`:
    *directoryPath* is invalid path or not full path. Invalid *pattern* (`"**options "` or regular expression).
- `DirectoryNotFoundException`:
    *directoryPath* directory does not exist.
- `Au.Types.AuException`:
    Failed to get children of *directoryPath* or of a subdirectory.

#### Remarks

Uses API `FindFirstFile`.

By default gets only direct children. Use flag `Au.Types.FEFlags.AllDescendants` to get all descendants.

The paths that this function gets are normalized, ie may not start with exact *directoryPath* string. Expanded environment variables (see `Au.pathname.expand`), `".."`, DOS path etc. Paths longer than `Au.pathname.maxDirectoryPathLength` have `@"\\?\"` prefix (see `Au.pathname.prefixLongPathIfNeed`).

For NTFS links (symbolic links, mount points) gets link info, not target info.

These errors are ignored:

1. Missing target directory of a NTFS link.
2. If used flag `Au.Types.FEFlags.IgnoreInaccessible` - access denied.

When an error is ignored, the function works as if that [sub]directory is empty; does not throw exception and does not call *errorHandler*.

Enumeration of a subdirectory starts immediately after the subdirectory itself is retrieved.