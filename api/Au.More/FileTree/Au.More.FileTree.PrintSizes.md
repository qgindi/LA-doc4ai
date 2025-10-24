# Method `Au.More.FileTree.PrintSizes`

## Overload 1

Appends to a `System.Text.StringBuilder` a list of sizes and names of descendants, formatted for `Au.print.it`, without a header.

```
public void PrintSizes(StringBuilder b)
```

##### Parameters

- *b*  (`StringBuilder`)

* * *

## Overload 2

Formats and prints a list of sizes and names of folder's descendant folders and optionally files, with a header.

```
public static void PrintSizes(string path, bool onlyDirectories = false, double minSizeMB = 0, bool ignoreInaccessible = true, bool recurseNtfsLinks = false, Func<FEFile, bool> dirFilter = null, Func<FEFile, bool> fileFilter = null)
```

##### Parameters

- *path*  (`string`):
    Folder path.
- *onlyDirectories*  (`bool`):
    Don't include files.
- *minSizeMB*  (`double`):
    Don't include smaller files and directories. The unit is MB.
- *ignoreInaccessible*  (`bool`):
    If cannot access some descendant directories, ignore them and don't throw exception. Default `true`.
- *recurseNtfsLinks*  (`bool`):
    Enumerate target directories of NTFS links, such as symbolic links and mount points.
- *dirFilter*  (`Func<Au.Types.FEFile, bool>`):
    Called for each descendant directory. If returns `false`, that directory with descendants is not included. But its size contributes to ancestor sizes anyway.
- *fileFilter*  (`Func<Au.Types.FEFile, bool>`):
    Called for each descendant file. If returns `false`, that file is not included. But its size contributes to ancestor sizes anyway.

##### Exceptions

- `Exception`:
    Exceptions of `Au.filesystem.enumerate`.