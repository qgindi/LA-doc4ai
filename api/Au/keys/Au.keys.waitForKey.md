# Method `Au.keys.waitForKey`

## Overload 1

Waits for key-down or key-up event of the specified key.

```
public static bool waitForKey(Seconds timeout, KKey key, bool up = false, bool block = false)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *key*  (`Au.Types.KKey`):
    Wait for this key.
- *up*  (`bool`):
    Wait for key-up event.
- *block*  (`bool`):
    Make the event invisible to other apps. If *up* is `true`, makes the down event invisible too, if it comes while waiting for the up event.

##### Returns

`bool`

Returns `true`. On timeout returns `false` if *timeout* is negative; else exception.

##### Exceptions

- `ArgumentException`:
    *key* is 0.
- `TimeoutException`:
    *timeout* time has expired (if > 0).

#### Remarks

Waits for key event, not for key state. Uses low-level keyboard hook. Can wait for any single key. See also `Au.keys.waitForHotkey`. Ignores key events injected by functions of this library.

#### Examples

```
keys.waitForKey(0, KKey.Ctrl, up: false, block: true);
print.it("Ctrl");
```

* * *

## Overload 2

Waits for key-down or key-up event of the specified key.

```
public static bool waitForKey(Seconds timeout, string key, bool up = false, bool block = false)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *key*  (`string`):
    Wait for this key. A single-key string. See [key names](../articles/Key%20names%20and%20operators.html).
- *up*  (`bool`):
    Wait for key-up event.
- *block*  (`bool`):
    Make the event invisible to other apps. If *up* is `true`, makes the down event invisible too, if it comes while waiting for the up event.

##### Returns

`bool`

Returns `true`. On timeout returns `false` if *timeout* is negative; else exception.

##### Exceptions

- `ArgumentException`:
    Invalid *key* string.
- `TimeoutException`:
    *timeout* time has expired (if > 0).

#### Remarks

Waits for key event, not for key state. Uses low-level keyboard hook. Can wait for any single key. See also `Au.keys.waitForHotkey`. Ignores key events injected by functions of this library.

#### Examples

```
keys.waitForKey(0, "Ctrl", up: false, block: true);
print.it("Ctrl");
```

* * *

## Overload 3

Waits for key-down or key-up event of any key, and gets the key code.

```
public static KKey waitForKey(Seconds timeout, bool up = false, bool block = false)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *up*  (`bool`):
    Wait for key-up event.
- *block*  (`bool`):
    Make the event invisible to other apps. If *up* is `true`, makes the down event invisible too, if it comes while waiting for the up event.

##### Returns

`Au.Types.KKey`

Returns the key code. On timeout returns 0 if *timeout* is negative; else exception. For modifier keys returns the left or right key code, for example `LCtrl`/`RCtrl`, not `Ctrl`.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).

#### Examples

```
var key = keys.waitForKey(0, up: true, block: true);
print.it(key);
```