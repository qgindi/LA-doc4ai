# Method `Au.mouse.waitForCursor`

## Overload 1

Waits for a standard mouse cursor (pointer) visible.

```
public static bool waitForCursor(Seconds timeout, MCursor cursor, bool not = false)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *cursor*  (`Au.Types.MCursor`):
    Id of a standard cursor.
- *not*  (`bool`):
    Wait until this cursor disappears.

##### Returns

`bool`

Returns `true`. On timeout returns `false` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).

* * *

## Overload 2

Waits for a nonstandard mouse cursor (pointer) visible.

```
public static bool waitForCursor(Seconds timeout, long cursorHash, bool not = false)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *cursorHash*  (`long`):
    Cursor hash, as returned by `Au.More.MouseCursor.Hash`.
- *not*  (`bool`):
    Wait until this cursor disappears.

##### Returns

`bool`

Returns `true`. On timeout returns `false` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).