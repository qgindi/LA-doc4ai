# Method `Au.keys.waitForNoModifierKeys`

Waits while some modifier keys (`Ctrl`, `Shift`, `Alt`, `Win`) are pressed. See `Au.keys.isMod`.

```
public static bool waitForNoModifierKeys(Seconds timeout = default, KMod mod = KMod.Shift | KMod.Ctrl | KMod.Alt | KMod.Win)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *mod*  (`Au.Types.KMod`):
    Check only these keys. Default: all.

##### Returns

`bool`

Returns `true`. On timeout returns `false` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).