# Method `Au.More.CpuUsage.OfProcess`

Gets CPU usage of a process.

```
public static double OfProcess(int processId, int duration = 10)
```

##### Parameters

- *processId*  (`int`):
    Process id.
- *duration*  (`int`):
    How long to measure, milliseconds. Default 10. Min 1. Calls `Thread.Sleep(duration);`.

##### Returns

`double`

CPU usage 0 to 100 %. Returns 0 if *processId* invalid.