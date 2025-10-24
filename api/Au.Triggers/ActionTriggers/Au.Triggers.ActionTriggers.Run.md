# Method `Au.Triggers.ActionTriggers.Run`

Makes triggers alive.

```
public void Run()
```

##### Exceptions

- `InvalidOperationException`:
    Already running.
- `Au.Types.AuException`:
    Something failed.

#### Remarks

This function monitors hotkeys, activated windows and other events. When an event matches an added trigger, launches the trigger's action, which runs in other thread by default. Does not return immediately. Runs until this process is terminated or `Au.Triggers.ActionTriggers.Stop` called.

#### Examples

See `Au.Triggers.ActionTriggers`.