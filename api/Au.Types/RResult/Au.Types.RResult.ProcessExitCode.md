# Property `Au.Types.RResult.ProcessExitCode`

The exit code of the process.

```
public int ProcessExitCode { get; }
```

##### Property Value

`int`

0 if no flag `WaitForExit` or if cannot wait.

#### Remarks

Usually the exit code is 0 or a process-defined error code.