# Constructor of `Au.More.CpuUsage`

## Overload 1

Use this constructor to get CPU usage of all processes (sum).

```
public CpuUsage()
```

* * *

## Overload 2

Use this constructor to get CPU usage of a process.

```
public CpuUsage(int processId)
```

##### Parameters

- *processId*  (`int`):
    Process id.

* * *

## Overload 3

Use this constructor to get CPU usage of multiple processes (sum).

```
public CpuUsage(IEnumerable<int> processes)
```

##### Parameters

- *processes*  (`IEnumerable<int>`):
    Process ids.