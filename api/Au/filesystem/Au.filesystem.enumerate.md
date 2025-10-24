# Method `Au.filesystem.enumerate`

Gets names and other info of files and subdirectories in the specified directory.

```
public static IEnumerable<FEFile> enumerate(string directoryPath, FEFlags flags = 0, Func<FEFile, bool> fileFilter = null, Func<FEFile, int> dirFilter = null, Action<string> errorHandler = null)
```

##### Parameters

- *directoryPath*  (`string`):
    Full path of the directory.
- *flags*  (`Au.Types.FEFlags`)
- *fileFilter*  (`Func<Au.Types.FEFile, bool>`):
    Callback function that is called for each file (but not subdirectory). Let it return `true` to include the file in results. Example: `f => f.Name.Ends(".png", true)`.
- *dirFilter*  (`Func<Au.Types.FEFile, int>`):
    Callback function that is called for each subdirectory. Let it return flags: 1 - include the directory in results; 2 - include its children in results. The return value overrides flags `Au.Types.FEFlags.OnlyFiles` and `Au.Types.FEFlags.AllDescendants`. Example: `d => d.Name.Eqi("Debug") ? 0 : 3`.
- *errorHandler*  (`Action<string>`):
    Callback function that is called when fails to get children of a subdirectory, when using flag `Au.Types.FEFlags.AllDescendants`. Receives the subdirectory path. Can call `Au.lastError.code` and throw an exception. If does not throw, the enumeration continues as if the directory is empty. If *errorHandler* not used, then `Au.filesystem.enumerate(string, FEFlags, Func<FEFile, bool>, Func<FEFile, int>, Action<string>)` throws exception. See also: flag `Au.Types.FEFlags.IgnoreInaccessible`.

##### Returns

`IEnumerable<Au.Types.FEFile>`

An enumerable collection of `Au.Types.FEFile` objects.

##### Exceptions

- `ArgumentException`:
    *directoryPath* is invalid path or not full path.
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