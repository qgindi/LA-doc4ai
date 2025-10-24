# Method `Au.More.CpuUsage.OfAllProcesses`

Gets CPU usage of all processes (sum).

```
public static double OfAllProcesses(int duration = 10)
```

##### Parameters

- *duration*  (`int`):
    How long to measure, milliseconds. Default 10. Min 1. Calls `Thread.Sleep(duration);`.

##### Returns

`double`

CPU usage 0 to 100 %.