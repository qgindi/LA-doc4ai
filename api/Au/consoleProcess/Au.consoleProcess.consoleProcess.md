# Constructor of `Au.consoleProcess`

Starts specified console program.

```csharp
public consoleProcess(string exe, string args = null, string curDir = null)
```

##### Parameters

- *exe*  (`string`):
  
  Path or name of an `.exe` or `.bat` file. Can be:
  
  - Full path. Examples: `@"C:\folder\abc.exe"`, `folders.System + "abc.exe"`, `@"%folders.System%\abc.exe"`.
  - Filename, like `"abc.exe"`. This function calls `Au.filesystem.searchPath`.
  - Path relative to `Au.folders.ThisApp`. Examples: `"abc.exe"`, `@"subfolder\abc.exe"`, `@".\subfolder\abc.exe"`, `@"..\folder\abc.exe"`.

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