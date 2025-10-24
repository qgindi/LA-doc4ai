# Method `Au.filesystem.more.getFinalPath`

Gets full normalized path of an existing file or directory or symbolic link target.

```
public static bool getFinalPath(string path, out string result, bool ofSymlink = false, FPFormat format = FPFormat.PrefixIfLong)
```

##### Parameters

- *path*  (`string`):
    Full or relative path. Supports environment variables (see `Au.pathname.expand`).
- *result*  (`string`):
    Receives full path, or `null` if failed.
- *ofSymlink*  (`bool`):
    If *path* is of a symbolic link, get final path of the link, not of its target.
- *format*  (`Au.Types.FPFormat`):
    Result format.

##### Returns

`bool`

`false` if failed. For example if the path does not point to an existing file or directory. Supports `Au.lastError`.

##### Exceptions

- `ArgumentException`:
    Not full path.

#### Remarks

Calls API `GetFinalPathNameByHandle`.

Unlike `Au.pathname.normalize`, this function works with existing files and directories, not any strings.

### See Also

`Au.shortcutFile.getTarget`