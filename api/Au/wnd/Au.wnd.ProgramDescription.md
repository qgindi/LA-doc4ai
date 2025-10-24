# Property `Au.wnd.ProgramDescription`

Gets description of process executable file.

```
public string ProgramDescription { get; }
```

##### Property Value

`string`

`null` if failed.

#### Remarks

Calls `Au.wnd.ProcessId` and `Au.process.getDescription`. This function is slow. Much slower than `Au.wnd.ProgramName`.