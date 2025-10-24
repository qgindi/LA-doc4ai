# Method `Au.filesystem.more.comparePaths`

## Overload 1

Compares final paths of two existing files or directories to determine equality or relationship.

```
public static CPResult comparePaths(string pathA, string pathB, bool ofSymlinkA = false, bool ofSymlinkB = false)
```

##### Parameters

- *pathA*  (`string`):
    Full or relative path of an existing file or directory, in any format. Supports environment variables (see `Au.pathname.expand`).
- *pathB*  (`string`):
    Full or relative path of an existing file or directory, in any format. Supports environment variables (see `Au.pathname.expand`).
- *ofSymlinkA*  (`bool`):
    If *pathA* is of a symbolic link, get final path of the link, not of its target.
- *ofSymlinkB*  (`bool`):
    If *pathB* is of a symbolic link, get final path of the link, not of its target.

##### Returns

`Au.Types.CPResult`

##### Exceptions

- `ArgumentException`:
    Not full path.

#### Remarks

Before comparing, calls `Au.filesystem.more.getFinalPath`, therefore paths can have any format. Example: `@"C:\Test\"` and `@"C:\A\..\Test"` are equal. Example: `@"C:\Test\file.txt"` and `"file.txt"` are equal if the file is in `@"C:\Test` and `@"C:\Test` is current directory. Example: `@"C:\Temp\file.txt"` and `"%TEMP%\file.txt"` are equal if `TEMP` is an environment variable = `@"C:\Temp`.

### See Also

`Au.filesystem.more.isSameFile`

* * *

## Overload 2

Compares final paths of two existing files or directories to determine equality or relationship. Also gets final paths (see `Au.filesystem.more.getFinalPath`).

```
public static CPResult comparePaths(ref string pathA, ref string pathB, bool ofSymlinkA = false, bool ofSymlinkB = false)
```

##### Parameters

- *pathA*  (`string`):
    Full or relative path of an existing file or directory, in any format. Supports environment variables (see `Au.pathname.expand`).
- *pathB*  (`string`):
    Full or relative path of an existing file or directory, in any format. Supports environment variables (see `Au.pathname.expand`).
- *ofSymlinkA*  (`bool`):
    If *pathA* is of a symbolic link, get final path of the link, not of its target.
- *ofSymlinkB*  (`bool`):
    If *pathB* is of a symbolic link, get final path of the link, not of its target.

##### Returns

`Au.Types.CPResult`

##### Exceptions

- `ArgumentException`:
    Not full path.

#### Remarks

Before comparing, calls `Au.filesystem.more.getFinalPath`, therefore paths can have any format. Example: `@"C:\Test\"` and `@"C:\A\..\Test"` are equal. Example: `@"C:\Test\file.txt"` and `"file.txt"` are equal if the file is in `@"C:\Test` and `@"C:\Test` is current directory. Example: `@"C:\Temp\file.txt"` and `"%TEMP%\file.txt"` are equal if `TEMP` is an environment variable = `@"C:\Temp`.

### See Also

`Au.filesystem.more.isSameFile`