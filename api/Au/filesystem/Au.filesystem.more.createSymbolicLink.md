# Method `Au.filesystem.more.createSymbolicLink`

Creates a NTFS symbolic link or junction.

```
public static void createSymbolicLink(string linkPath, string targetPath, CSLink type, bool elevate = false, bool deleteOld = false)
```

##### Parameters

- *linkPath*  (`string`):
    Full path of the link. Supports environment variables etc.
- *targetPath*  (`string`):
    If *type* is `Junction`, must be full path. Else can be either full path or path relative to the parent directory of the link. If starts with an environment variable, the function expands it before creating the link.
- *type*  (`Au.Types.CSLink`)
- *elevate*  (`bool`):
    If fails to create symbolic link because this process does not have admin rights, run `cmd.exe mklink` as administrator. Will show a dialog and UAC consent. Not used if type is `Junction`, because don't need admin rights to create junctions.
- *deleteOld*  (`bool`):
    If *linkPath* already exists as a symbolic link or junction or empty directory, replace it.

##### Exceptions

- `ArgumentException`:
    Not full path.
- `Au.Types.AuException`:
    Failed.

#### Remarks

Some reasons why this function can fail:

- The link already exists. Solution: use `deleteOld: true`.
- This process is running not as administrator. Solution: use *type* `Junction` or `elevate: true`. To create symbolic links without admin rights, in Windows Settings enable developer mode.
- The file system format is not NTFS. For example FAT32 in USB drive.

More info: [CreateSymbolicLink, mklink, NTFS symbolic links, junctions](https://www.google.com/search?q=CreateSymbolicLink%2C+mklink%2C+NTFS+symbolic+links%2C+junctions).