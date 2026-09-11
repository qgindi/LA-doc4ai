# Constructor of `Au.More.CpuUsage`

## Overload 1

Use this constructor to get CPU usage of all processes (sum).

```csharp
public CpuUsage()
```

* * *

## Overload 2

Use this constructor to get CPU usage of a process.

```csharp
public CpuUsage(int processId)
```

##### Parameters

- *processId*  (`int`):
  Process id.

* * *

## Overload 3

Use this constructor to get CPU usage of multiple processes (sum).

```csharp
public CpuUsage(IEnumerable<int> processes)
```

##### Parameters

- *processes*  (`IEnumerable<int>`):
  Process ids.