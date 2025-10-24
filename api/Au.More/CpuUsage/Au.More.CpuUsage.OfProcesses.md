# Method `Au.More.CpuUsage.OfProcesses`

Gets CPU usage of multiple processes (sum).

```
public static double OfProcesses(IEnumerable<int> processes, int duration = 10)
```

##### Parameters

- *processes*  (`IEnumerable<int>`):
    Process ids.
- *duration*  (`int`):
    How long to measure, milliseconds. Default 10. Min 1. Calls `Thread.Sleep(duration);`.

##### Returns

`double`

CPU usage 0 to 100 %. Returns 0 if all ids invalid.