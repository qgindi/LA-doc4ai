# Method `Au.filesystem.save`

Writes any data to a file in a safe way, using a callback function.

```
public static void save(string file, Action<string> writer, bool backup = false, string tempDirectory = null, int lockedWaitMS = 2000)
```

##### Parameters

- *file*  (`string`):
    File. Must be full path. Can contain environment variables etc, see `Au.pathname.expand`. If the file exists, this function overwrites it. If the directory does not exist, this function creates it.
- *writer*  (`Action<string>`):
    Callback function (lambda etc) that creates/writes/closes a temporary file. Its parameter is the full path of the temporary file, which normally does not exist. May be called multiple times, because this function retries if the file is locked or if the directory does not exist (if *writer* throws `System.IO.DirectoryNotFoundException` exception).
- *backup*  (`bool`):
    Create backup file named *file* + `"~backup"`.
- *tempDirectory*  (`string`):
    Directory for backup file and temporary file. If `null` or `""` - *file*'s directory. Can contain environment variables etc. Must be in the same drive as *file*. If the directory does not exist, this function creates it.
- *lockedWaitMS*  (`int`):
    If cannot open the file because it is opened by another process etc, wait max this number of milliseconds. Can be `System.Threading.Timeout.Infinite` (-1).

##### Exceptions

- `ArgumentException`:
    Invalid *file* (eg not full path) or *lockedWaitMS* (less than -1).
- `IOException`:
    Failed to replace file.
- `Exception`:
    Exceptions of the function that actually writes data.

#### Remarks

The file-write functions provided by .NET and Windows API are less reliable, because:

1. Fails if the file is temporarily open by another process or thread without sharing.
2. Can corrupt file data. If this thread, process, PC or disk dies while writing, may write only part of data or just make empty file. Usually it happens when PC is turned off incorrectly.

To protect from 1, this functions waits/retries if the file is temporarily open/locked, like `Au.filesystem.waitIfLocked`. To protect from 2, this function writes to a temporary file and renames/replaces the specified file using API `ReplaceFile`. Although not completely atomic, it ensures that file data is not corrupt; if cannot write all data, does not change existing file data. Also this function auto-creates directory if does not exist.

This function is slower. Speed can be important when saving many files.