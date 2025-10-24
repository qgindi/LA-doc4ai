# Method `Au.csvTable.Save`

Composes CSV and saves to a file.

```
public void Save(string file, bool backup = false)
```

##### Parameters

- *file*  (`string`):
    File. Must be full path. Can contain environment variables etc, see `Au.pathname.expand`. The file can exist or not; this function overwrites it.
- *backup*  (`bool`):
    Create backup file named `file + "~backup"`.

##### Exceptions

- `ArgumentException`:
    Not full path.
- `Exception`:
    Exceptions of `System.IO.File.WriteAllText`.

#### Remarks

Calls `Au.csvTable.ToString` and `System.IO.File.WriteAllText`. Also uses `Au.filesystem.save`.