# Method `Au.keys.waitForReleased`

## Overload 1

Waits while the specified keys or/and mouse buttons are pressed.

```csharp
public static bool waitForReleased(Seconds timeout, params KKey[] keys_)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
  Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](🔗).
- *keys_*  (`Au.Types.KKey[]`):
  One or more keys or/and mouse buttons. Waits until all are released.

##### Returns

`bool`

Returns `true`. On timeout returns `false` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
  *timeout* time has expired (if > 0).

* * *

## Overload 2

Waits while the specified keys are pressed.

```csharp
public static bool waitForReleased(Seconds timeout, string keys_)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
  Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](🔗).
- *keys_*  (`string`):
  One or more [keys](🔗) without operators. Waits until all are released.

##### Returns

`bool`

Returns `true`. On timeout returns `false` if *timeout* is negative; else exception.

##### Exceptions

- `ArgumentException`:
  Error in *keys_* string.
- `TimeoutException`:
  *timeout* time has expired (if > 0).