# Property `Au.wnd.ProgramName`

Gets filename of process executable file, like `"notepad.exe"`.

```
public string ProgramName { get; }
```

##### Property Value

`string`

`null` if failed.

#### Remarks

Calls `Au.wnd.ProcessId` and `Au.process.getName`. This function is much slower than getting window name or class name. Don't use code like `if(w.ProgramName=="A" || w.ProgramName=="B")`. Instead use `var s=w.ProgramName; if(s=="A" || s=="B")`.