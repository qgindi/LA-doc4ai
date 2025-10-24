# Method `Au.More.AppSingleInstance.AlreadyRunning`

Detects whether a process of this app is already running.

```
public static bool AlreadyRunning(string mutex, IEnumerable<string> notifyArgs = null, int waitMS = 0)
```

##### Parameters

- *mutex*  (`string`):
    A unique string to use for mutex name (see `System.Threading.Mutex.Mutex`). If prefix `@"Global\"` used, detects processes in all user sessions.
- *notifyArgs*  (`IEnumerable<string>`):

    If not `null`:

    - If already running, sends it to that process, which receives it in `Au.More.AppSingleInstance.Notified` event.
    - Else enables `Au.More.AppSingleInstance.Notified` event in this process.
- *waitMS*  (`int`):
    Milliseconds to wait until this process can run. No timeout if -1.

##### Returns

`bool`

True if already running.

##### Exceptions

- `InvalidOperationException`:
    This function already called.
- `Exception`:
    Exceptions of `System.Threading.Mutex.Mutex`.