# Method `Au.mouse.waitForClick`

## Overload 1

Waits for button-down or button-up event of the specified mouse button or buttons.

```
public static bool waitForClick(Seconds timeout, MButtons button, bool up = false, bool block = false)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *button*  (`Au.Types.MButtons`):
    Mouse button. If several buttons specified, waits for any of them.
- *up*  (`bool`):
    Wait for button-up event.
- *block*  (`bool`):
    Make the event invisible to other apps. If *up* is `true`, makes the down event invisible too, if it comes while waiting for the up event.

##### Returns

`bool`

Returns `true`. On timeout returns `false` if *timeout* is negative; else exception.

##### Exceptions

- `ArgumentException`:
    *button* is 0.
- `TimeoutException`:
    *timeout* time has expired (if > 0).

#### Remarks

Unlike `Au.mouse.waitForNoButtonsPressed`, waits for down or up event, not for button state. Uses low-level mouse hook. Ignores mouse events injected by functions of this library.

#### Examples

```
mouse.waitForClick(0, MButtons.Left, up: true, block: false);
print.it("click");
```

* * *

## Overload 2

Waits for button-down or button-up event of any mouse button, and gets the button code.

```
public static MButtons waitForClick(Seconds timeout, bool up = false, bool block = false)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *up*  (`bool`):
    Wait for button-up event.
- *block*  (`bool`):
    Make the event invisible to other apps. If *up* is `true`, makes the down event invisible too, if it comes while waiting for the up event.

##### Returns

`Au.Types.MButtons`

Returns the button code. On timeout returns 0 if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).

#### Examples

```
var button = mouse.waitForClick(0, up: true, block: true);
print.it(button);
```