# Method `Au.More.WaitableTimer.Open`

Calls API `OpenWaitableTimer` and creates a `Au.More.WaitableTimer` object that wraps the timer handle.

```csharp
public static WaitableTimer Open(string timerName, uint access = 1048578, bool inheritHandle = false, bool noException = false)
```

##### Parameters

- *timerName*  (`string`):
  Timer name. Fails if it does not exist; to open-or-create use `Au.More.WaitableTimer.Create`.
- *access*  (`uint`):
  See [Synchronization Object Security and Access Rights](🔗). The default value `TIMER_MODIFY_STATE|SYNCHRONIZE` allows to set and wait.
- *inheritHandle*  (`bool`)
- *noException*  (`bool`):
  If fails, return `null`, don't throw exception. Supports `Au.lastError`.

##### Returns

`Au.More.WaitableTimer`

##### Exceptions

- `Au.Types.AuException`:
  Failed. For example, the timer does not exist.