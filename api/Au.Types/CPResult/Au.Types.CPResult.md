# Enum `Au.Types.CPResult`

See `Au.filesystem.more.comparePaths`.

```
public enum CPResult
```

### Fields

| Name | Description |
| --- | --- |
| AContainsB | *pathA* is of a directory that contains file or directory specified by *pathB*. Example: `pathA: @"C:\Dir1"`, `pathB: @"C:\Dir1\Dir2\File1.txt"`. |
| BContainsA | *pathB* is of a directory that contains file or directory specified by *pathA*. Example: `pathA: @"C:\Dir1\Dir2\File1.txt"`, `pathB: @"C:\Dir1"`. |
| Failed | Failed. Probably one (or both) of specified files does not exist. The function supports `Au.lastError`. |
| None | The paths are unrelated. Example: `pathA: @"C:\Dir1\File1.txt"`, `pathB: @"C:\Dir2\File1.txt"`. |
| Same | Both paths are of the same file or directory. Example: `pathA: @"C:\Dir1\File1.txt"`, `pathB: @"C:\Dir2\..\Dir1\File1.txt"`. |