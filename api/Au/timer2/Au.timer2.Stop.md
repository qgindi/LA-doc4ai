# Method `Au.timer2.Stop`

Stops the timer, and by default disposes.

```
public void Stop(bool canReuse = false)
```

##### Parameters

- *canReuse*  (`bool`):
    Just stop but don't dispose. If `false` (default), can't use the timer again.