# Method `Au.mouse.waitForNoButtonsPressed`

Waits while some mouse buttons are pressed. See `Au.mouse.isPressed`.

```
public static bool waitForNoButtonsPressed(Seconds timeout = default, MButtons buttons = MButtons.Left | MButtons.Right | MButtons.Middle | MButtons.X1 | MButtons.X2)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html). Default 0.
- *buttons*  (`Au.Types.MButtons`):
    Wait only for these buttons. Default - all.

##### Returns

`bool`

Returns `true`. On timeout returns `false` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).

### See Also

`Au.keys.waitForNoModifierKeysAndMouseButtons`