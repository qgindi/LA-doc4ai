# Method `Au.process.getTimes`

Gets process creation and execution times (API `GetProcessTimes`).

```
public static bool getTimes(int processId, out long created, out long executed)
```

##### Parameters

- *processId*  (`int`):
    Process id.
- *created*  (`long`):
    Creation time. As absolute `FILETIME`, UTC. If you need `System.DateTime`, use `System.DateTime.FromFileTimeUtc`.
- *executed*  (`long`):
    Amount of time spent executing code (using CPU). As `FILETIME`. If you need `System.TimeSpan`, use `System.TimeSpan.FromTicks`.

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.