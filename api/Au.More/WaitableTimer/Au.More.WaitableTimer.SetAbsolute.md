# Method `Au.More.WaitableTimer.SetAbsolute`

Calls API `SetWaitableTimer`.

```
public bool SetAbsolute(DateTime dueTime, int period = 0)
```

##### Parameters

- *dueTime*  (`DateTime`):
    The UTC date/time at which the state of the timer is to be set to signaled.
- *period*  (`int`):
    The period of the timer, in milliseconds. If 0, the timer is signaled once. If greater than 0, the timer is periodic.

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.