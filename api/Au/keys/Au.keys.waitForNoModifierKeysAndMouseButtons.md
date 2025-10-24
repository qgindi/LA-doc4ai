# Method `Au.keys.waitForNoModifierKeysAndMouseButtons`

Waits while some modifier keys (`Ctrl`, `Shift`, `Alt`, `Win`) or mouse buttons are pressed.

```
public static bool waitForNoModifierKeysAndMouseButtons(Seconds timeout = default, KMod mod = KMod.Shift | KMod.Ctrl | KMod.Alt | KMod.Win, MButtons buttons = MButtons.Left | MButtons.Right | MButtons.Middle | MButtons.X1 | MButtons.X2)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html). Default 0.
- *mod*  (`Au.Types.KMod`):
    Check only these keys. Default: all.
- *buttons*  (`Au.Types.MButtons`):
    Check only these buttons. Default: all.

##### Returns

`bool`

Returns `true`. On timeout returns `false` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).

### See Also

`Au.keys.isMod`

`Au.mouse.isPressed`

`Au.mouse.waitForNoButtonsPressed`