# Class `Au.filesystem`

File and directory functions. Copy, move, delete, find, get properties, enumerate, create directory, load/save, etc.

```
public static class filesystem
```

##### Remarks

Also you can use .NET file system classes, such as `System.IO.File` and `System.IO.Directory` in `System.IO` namespace. In the past they were too limited and unsafe to use, for example no long paths, too many exceptions, difficult to recursively enumerate directories containing protected items. Later improved, but this class still has something they don't, for example environment variables in path, safe load/save. This class does not have low-level functions to open/read/write files.

Most functions support only full path. Most of them throw `System.ArgumentException` if passed a filename or relative path, ie in "current directory". Using current directory is unsafe. Most functions support extended-length paths (longer than 259). Such local paths should have `@"\\?\"` prefix, like `@"\\?\C:\..."`. Such network path should be like `@"\\?\UNC\server\share\..."`. See `Au.pathname.prefixLongPath`, `Au.pathname.prefixLongPathIfNeed`. Many functions support long paths even without prefix.

Disk drives like `@"C:\"` or `"C:"` are directories too.

##### Inheritance

`object` → `filesystem`

### Methods

`copy`, `copyTo`, `createDirectory`, `createDirectoryFor`, `delete`, `delete`, `enumDirectories`, `enumFiles`, `enumerate`, `exists`, `getAttributes`, `getProperties`, `loadBytes`, `loadStream`, `loadText`, `move`, `moveTo`, `rename`, `save`, `saveBytes`, `saveText`, `searchPath`, `setAttributes`, `waitIfLocked`, `waitIfLocked<T>`