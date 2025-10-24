# Method `Au.filesystem.loadText`

Loads text file in a safer way. Uses `System.IO.File.ReadAllText` and `Au.filesystem.waitIfLocked<T>`.

```
public static string loadText(string file, Encoding encoding = null, int lockedWaitMS = 2000, int missingWaitMS = 0)
```

##### Parameters

- *file*  (`string`):
    File. Must be full path. Can contain environment variables etc, see `Au.pathname.expand`.
- *encoding*  (`Encoding`):
    Text encoding in file (if there is no BOM). Default UTF-8.
- *lockedWaitMS*  (`int`):
    If cannot open the file because it is opened by another process etc, wait max this number of milliseconds. Can be `System.Threading.Timeout.Infinite` (-1).
- *missingWaitMS*  (`int`):
    If the file initially does not exist, wait max this number of milliseconds until exists. Can be `System.Threading.Timeout.Infinite` (-1).

##### Returns

`string`

##### Exceptions

- `ArgumentException`:
    Not full path.
- `ArgumentOutOfRangeException`:
    A timeout is less than -1.
- `TimeoutException`:
    *missingWaitMS* is > 0 and the file still does not exist after waiting.
- `Exception`:
    Exceptions of `System.IO.File.ReadAllText`.