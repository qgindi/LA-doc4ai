# Method `Au.keys.AddSleep`

Adds a short pause. Then `Au.keys.SendNow` will sleep (wait).

```
public keys AddSleep(int timeMS)
```

##### Parameters

- *timeMS*  (`int`):
    Time to sleep, milliseconds.

##### Returns

`Au.keys`

This.

##### Exceptions

- `ArgumentOutOfRangeException`:
    *timeMS* >10000 (1 minute) or \<0.