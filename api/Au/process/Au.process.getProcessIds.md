# Method `Au.process.getProcessIds`

Gets process ids of all processes of the specified program.

```
public static int[] getProcessIds(string processName, bool? fullPath = false, bool ofThisSession = false)
```

##### Parameters

- *processName*  (`string`):
    Process executable file name, like `"notepad.exe"`. String format: [wildcard expression](../articles/Wildcard%20expression.html).
- *fullPath*  (`bool?`):
    *processName* is full path. If `null`, calls `Au.pathname.isFullPathExpand`. Note: Fails to get full path if the process belongs to another user session, unless current process is running as administrator; also fails to get full path of some system processes.
- *ofThisSession*  (`bool`):
    Get processes only of this user session.

##### Returns

`int[]`

Array containing zero or more elements.

##### Exceptions

- `ArgumentException`:

    - *processName* is `""` or `null`.
    - Invalid wildcard expression (`"**options "` or regular expression).