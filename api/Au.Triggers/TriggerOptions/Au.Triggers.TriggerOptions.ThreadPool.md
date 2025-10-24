# Method `Au.Triggers.TriggerOptions.ThreadPool`

Run trigger actions in thread pool threads.

```
public void ThreadPool(bool single = false)
```

##### Parameters

- *single*  (`bool`):
    Don't run if this action is already running. If `false`, multiple action instances can run parallelly in multiple threads.

#### Remarks

The action can run simultaneously with other actions. May start later if the pool is busy. You should know how to use thread pool correctly. The action runs in the .NET thread pool through `System.Threading.Tasks.Task.Run`.