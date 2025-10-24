# Method `Au.Triggers.ActionTrigger.RunAction`

Starts the action like when its trigger is activated.

```
public void RunAction(TriggerArgs args)
```

##### Parameters

- *args*  (`Au.Triggers.TriggerArgs`)

##### Exceptions

- `InvalidOperationException`:
    Called before or after `Au.Triggers.ActionTriggers.Run`.

#### Remarks

This function must be called while the main triggers thread is in `Au.Triggers.ActionTriggers.Run`, for example from another trigger action. It is asynchronous (does not wait). If called from a trigger action (hotkey etc), make sure this action runs in another thread or can be queued. Else both actions cannot run simultaneously.