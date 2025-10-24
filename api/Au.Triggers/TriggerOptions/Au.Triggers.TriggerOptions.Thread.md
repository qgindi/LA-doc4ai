# Method `Au.Triggers.TriggerOptions.Thread`

Run actions always in the same dedicated thread that does not end when actions end.

```
public void Thread(int thread = 0, int wait = 0, bool noWarning = false)
```

##### Parameters

- *thread*  (`int`):
    A number that you want to use to identify the thread. Can be 0-127. Default 0.
- *wait*  (`int`):
    Defines when to start an action if an action (other or same) is currently running in this thread. If 0 (default), don't run. If -1 (`Timeout.Infinite`), run when that action ends (and possibly other queued actions). If > 0, run when that action ends, if it ends within this time from now; the time is in milliseconds.
- *noWarning*  (`bool`):
    No warning when cannot start an action because an action is running and *wait* == 0.

##### Exceptions

- `ArgumentOutOfRangeException`

#### Remarks

Multiple actions in same thread cannot run simultaneously. Actions in different threads can run simultaneously. There is no "end old running action" feature. If need it, use other script. Example: `Triggers.Hotkey["Ctrl+M"] = o => script.runWait("Other Script");`. There is no "temporarily pause old running action to run new action" feature. As well as for scripts. The thread has `System.Threading.ApartmentState.STA`. There are several `ThreadX` functions. Only the last called function is active. If none called, it is the same as called this function without arguments.