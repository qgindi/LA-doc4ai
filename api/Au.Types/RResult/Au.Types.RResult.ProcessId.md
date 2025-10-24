# Property `Au.Types.RResult.ProcessId`

The process id.

```
public int ProcessId { get; }
```

##### Property Value

`int`

0 if used flag `WaitForExit` or if did not start new process (eg opened the document in an existing process) or if cannot get it.