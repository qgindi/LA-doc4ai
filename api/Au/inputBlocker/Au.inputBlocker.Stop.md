# Method `Au.inputBlocker.Stop`

Stops blocking. Plays back blocked keys if need. See `Au.inputBlocker.ResendBlockedKeys`. Does nothing if currently is not blocking.

```
public void Stop(bool discardBlockedKeys = false)
```

##### Parameters

- *discardBlockedKeys*  (`bool`):
    Do not play back blocked key-down events recorded because of `Au.inputBlocker.ResendBlockedKeys`.