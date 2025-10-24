# Method `Au.filesystem.createDirectory`

Creates new directory if does not exists. If need, creates missing parent/ancestor directories.

```
public static bool createDirectory(string path, string templateDirectory = null)
```

##### Parameters

- *path*  (`string`):
    Path of new directory.
- *templateDirectory*  (`string`):
    Optional path of a template directory from which to copy some properties. See API `CreateDirectoryEx`.

##### Returns

`bool`

`true` if created new directory, `false` if the directory already exists. Throws exception if failed.

##### Exceptions

- `ArgumentException`:
    Not full path.
- `Au.Types.AuException`:
    Failed.

#### Remarks

If the directory already exists, this function does nothing, and returns `false`. Else, at first it creates missing parent/ancestor directories, then creates the specified directory. To create the specified directory, calls API `CreateDirectory` or `CreateDirectoryEx` (if *templateDirectory* is not `null`).