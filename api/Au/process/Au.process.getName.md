# Method `Au.process.getName`

Gets process executable file name (like `"notepad.exe"`) or full path.

```
public static string getName(int processId, bool fullPath = false, bool noSlowAPI = false)
```

##### Parameters

- *processId*  (`int`):
    Process id.
- *fullPath*  (`bool`):
    Get full path. Note: Fails to get full path if the process belongs to another user session, unless current process is running as administrator; also fails to get full path of some system processes.
- *noSlowAPI*  (`bool`):
    When the fast API `QueryFullProcessImageName` fails, don't try to use another much slower API `WTSEnumerateProcesses`. Not used if *fullPath* is `true`.

##### Returns

`string`

`null` if failed.

#### Remarks

This function is much slower than getting window name or class name.

### See Also

`Au.wnd.ProgramName`

`Au.wnd.ProgramPath`

`Au.wnd.ProcessId`