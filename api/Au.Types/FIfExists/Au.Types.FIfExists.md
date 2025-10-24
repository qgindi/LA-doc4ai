# Enum `Au.Types.FIfExists`

What to do if the destination directory contains a file or directory with the same name as the source file or directory when copying, moving or renaming.

```
public enum FIfExists
```

##### Remarks

Used with `Au.filesystem.copy`, `Au.filesystem.move` and similar functions. When renaming or moving, if the destination is the same as the source, these options are ignored and the destination is simply renamed. For example when renaming `"file.txt"` to `"FILE.TXT"`.

### Fields

| Name | Description |
| --- | --- |
| Delete | Delete destination. |
| Fail | Throw exception. Default. |
| MergeDirectory | If destination directory exists, merge the source directory into it, replacing existing files. If destination file exists, deletes it. If destination directory exists and source is file, fails. |
| RenameExisting | Rename (backup) destination. |
| RenameNew | Copy/move with a different name. |