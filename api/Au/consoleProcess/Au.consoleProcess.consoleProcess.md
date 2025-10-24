# Constructor of `Au.consoleProcess`

Starts the console program.

```
public consoleProcess(string exe, string args = null, string curDir = null)
```

##### Parameters

- *exe*  (`string`):

    Path or name of an `.exe` or `.bat` file. Can be:

    - Full path. Examples: `@"C:\folder\x.exe"`, `folders.System + "x.exe"`, `@"%folders.System%\x.exe"`.
    - Filename, like `"x.exe"`. This function calls `Au.filesystem.searchPath`.
    - Path relative to `Au.folders.ThisApp`. Examples: `"x.exe"`, `@"subfolder\x.exe"`, `@".\subfolder\x.exe"`, `@"..\folder\x.exe"`.

Supports environment variables, like `@"%TMP%\x.bat"`. See `Au.pathname.expand`.
- *args*  (`string`):
    `null` or command line arguments.
- *curDir*  (`string`):

    Initial current directory of the new process.

    - If `null`, uses `Directory.GetCurrentDirectory()`.
    - Else if `""`, calls `pathname.getDirectory(exe)`.
    - Else calls `Au.pathname.expand`.

##### Exceptions

- `Au.Types.AuException`:
    Failed, for example file not found.