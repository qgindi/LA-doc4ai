# Method `Au.More.FileTree.Create`

Calls `Au.filesystem.enumerate` and creates a tree of descendants.

```
public static FileTree Create(string path, bool onlyDirectories = false, long minSize = 0, bool ignoreInaccessible = true, bool recurseNtfsLinks = false, Func<FEFile, bool> dirFilter = null, Func<FEFile, bool> fileFilter = null)
```

##### Parameters

- *path*  (`string`):
    Folder path.
- *onlyDirectories*  (`bool`):
    Don't include files.
- *minSize*  (`long`):
    Don't include smaller files and directories. The unit is bytes.
- *ignoreInaccessible*  (`bool`):
    If cannot access some descendant directories, ignore them and don't throw exception. Default `true`.
- *recurseNtfsLinks*  (`bool`):
    Enumerate target directories of NTFS links, such as symbolic links and mount points.
- *dirFilter*  (`Func<Au.Types.FEFile, bool>`):
    Called for each descendant directory. If returns `false`, that directory with descendants is not included. But its size contributes to ancestor sizes anyway.
- *fileFilter*  (`Func<Au.Types.FEFile, bool>`):
    Called for each descendant file. If returns `false`, that file is not included. But its size contributes to ancestor sizes anyway.

##### Returns

`Au.More.FileTree`

The root of the tree. You can use its descendants and `Au.More.FileTree.Size`. Don't use `Au.More.FileTree.Info`, `Au.More.FileTree.Name`, `Au.More.FileTree.Path` and `Au.More.FileTree.IsDirectory`.

##### Exceptions

- `Exception`:
    Exceptions of `Au.filesystem.enumerate`.