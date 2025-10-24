# Method `Au.filesystem.createDirectoryFor`

Creates parent directory for a new file, if does not exist. The same as `Au.filesystem.createDirectory`, just removes filename from *filePath*.

```
public static bool createDirectoryFor(string filePath)
```

##### Parameters

- *filePath*  (`string`):
    Path of new file.

##### Returns

`bool`

`true` if created new directory, `false` if the directory already exists. Throws exception if failed.

##### Exceptions

- `ArgumentException`:
    Not full path. No filename.
- `Au.Types.AuException`:
    Failed.

#### Examples

```
string path = @"D:\Test\new\test.txt";
filesystem.createDirectoryFor(path);
File.WriteAllText(path, "text"); //would fail if directory @"D:\Test\new" does not exist
```