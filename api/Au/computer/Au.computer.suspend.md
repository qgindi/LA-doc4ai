# Method `Au.computer.suspend`

Computer sleep, hibernate or monitor off.

```csharp
public static bool suspend(CSuspend how)
```

##### Parameters

- *how*  (`Au.Types.CSuspend`):
  Enum: Sleep, Hibernate, Display, SleepOrDisplay.

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.

#### Remarks

To sleep or hibernate uses API `SetSuspendState`. To turn off display uses `WM_SYSCOMMAND`.

The `SetSuspendState` behavior is undefined if the system does not support S1-S3 sleep or S4 hibernate power states. It may fail or use hibernation instead of sleep. About power states: [System Power States](🔗). Available sleep states: `run.console("powercfg.exe", "/A");`