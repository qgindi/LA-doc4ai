# Method `Au.timer.Stop`

Stops the timer.

```
public void Stop()
```

##### Exceptions

- `InvalidOperationException`:
    Called not in the same thread as previously.

#### Remarks

The callback function will not be called after this. Later you can start the timer again (call `Au.timer.After` or `Au.timer.Every`). Don't need to call this function for single-period timers. For periodic timers it is optional; the timer stops when the thread ends. This function must be called in the same thread as `Au.timer.After` or `Au.timer.Every`.