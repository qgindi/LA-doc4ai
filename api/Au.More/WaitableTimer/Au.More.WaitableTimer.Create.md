# Method `Au.More.WaitableTimer.Create`

Calls API `CreateWaitableTimer` and creates a `Au.More.WaitableTimer` object that wraps the timer handle.

```
public static WaitableTimer Create(bool manualReset = false, string timerName = null)
```

##### Parameters

- *manualReset*  (`bool`)
- *timerName*  (`string`):
    Timer name. If a timer with this name already exists, opens it if possible. If `null`, creates unnamed timer.

##### Returns

`Au.More.WaitableTimer`

##### Exceptions

- `Au.Types.AuException`:
    Failed. For example, a non-timer kernel object with this name already exists.