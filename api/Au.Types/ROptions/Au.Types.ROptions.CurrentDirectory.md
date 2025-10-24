# Field `Au.Types.ROptions.CurrentDirectory`

Initial current directory for the new process. If `null` (default), the new process will inherit the current directory of this process. If `""`, the function gets parent directory path from the *file* parameter, if possible (if full path is specified or found); if not possible, same as `null`.

```
public string CurrentDirectory
```