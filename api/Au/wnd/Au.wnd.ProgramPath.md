# Property `Au.wnd.ProgramPath`

Gets full path of process executable file.

```
public string ProgramPath { get; }
```

##### Property Value

`string`

`null` if failed.

#### Remarks

Calls `Au.wnd.ProcessId` and `Au.process.getName`. This function is much slower than getting window name or class name. Don't use code like `if(w.ProgramPath=="A" || w.ProgramPath=="B")`. Instead use `var s=w.ProgramPath; if(s=="A" || s=="B")`.