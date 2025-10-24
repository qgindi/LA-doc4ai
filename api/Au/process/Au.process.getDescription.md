# Method `Au.process.getDescription`

Gets description of process executable file.

```
public static string getDescription(int processId)
```

##### Parameters

- *processId*  (`int`):
    Process id.

##### Returns

`string`

`null` if failed.

#### Remarks

Calls `Au.process.getVersionInfo` and `System.Diagnostics.FileVersionInfo.FileDescription`.