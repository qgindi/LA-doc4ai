# Method `Au.More.WaitableTimer.Set`

Calls API `SetWaitableTimer`.

```
public bool Set(long dueTime, int period = 0)
```

##### Parameters

- *dueTime*  (`long`):
    The time after which the state of the timer is to be set to signaled. It is relative time (from now). If positive, in milliseconds. If negative, in 100 nanosecond intervals (microseconds `*` 10), see `FILETIME`. Also can be 0, to set minimal time.
- *period*  (`int`):
    The period of the timer, in milliseconds. If 0, the timer is signaled once. If greater than 0, the timer is periodic.

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.

##### Exceptions

- `OverflowException`:
    `dueTime*10000` is greater than `System.Int64.MaxValue`.