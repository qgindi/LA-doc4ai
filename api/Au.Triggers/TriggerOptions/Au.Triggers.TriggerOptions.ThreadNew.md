# Method `Au.Triggers.TriggerOptions.ThreadNew`

Run trigger actions in new threads.

```
public void ThreadNew(bool single = false)
```

##### Parameters

- *single*  (`bool`):
    Don't run if this action is already running. If `false`, multiple action instances can run parallelly in multiple threads.

#### Remarks

The action can run simultaneously with other actions. The thread is STA.