# Method `Au.filesystem.more.getFileId`

Gets `Au.Types.FileId` of a file or directory.

```
public static bool getFileId(string path, out FileId fileId, bool ofSymlink = false)
```

##### Parameters

- *path*  (`string`):
    Path of a file or directory. Supports environment variables (see `Au.pathname.expand`) and paths relative to current directory.
- *fileId*  (`Au.Types.FileId`)
- *ofSymlink*  (`bool`):
    If *path* is of a symbolic link, get `Au.Types.FileId` of the link, not of its target.

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.

##### Exceptions

- `ArgumentException`:
    Not full path.

#### Remarks

Calls API `GetFileInformationByHandle`.

A file id can be used to uniquely identify a file or directory regardless of path format.

Note: later the function can get a different id for the same path. For example after deleting the file and then creating new file at the same path (some apps save files in this way). You may want to use `Au.filesystem.more.getFinalPath` instead.