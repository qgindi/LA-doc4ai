# Method `Au.keys.waitForHotkey`

Registers a temporary hotkey and waits for it.

```
public static bool waitForHotkey(Seconds timeout, KHotkey hotkey, bool waitModReleased = false)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *hotkey*  (`Au.Types.KHotkey`):
    Hotkey. Can be: string like `"Ctrl+Shift+Alt+Win+K"`, tuple `(KMod, KKey)`, enum `Au.Types.KKey`, enum `Keys`, struct `Au.Types.KHotkey`.
- *waitModReleased*  (`bool`):
    Also wait until hotkey modifier keys released.

##### Returns

`bool`

Returns `true`. On timeout returns `false` if *timeout* is negative; else exception.

##### Exceptions

- `ArgumentException`:
    Error in hotkey string.
- `Au.Types.AuException`:
    Failed to register hotkey.
- `TimeoutException`:
    *timeout* time has expired (if > 0).

#### Remarks

Uses `Au.More.RegisteredHotkey` (API `RegisterHotKey`). Fails if the hotkey is currently registered by this or another application or used by Windows.

> **Note:**
> Most single-key and `Shift+key` hotkeys don't work when the active window has higher UAC integrity level than this process. Media keys may work.

#### Examples

```
keys.waitForHotkey(0, "F11");
keys.waitForHotkey(0, KKey.F11);
keys.waitForHotkey(0, "Shift+A", true);
keys.waitForHotkey(0, (KMod.Ctrl | KMod.Shift, KKey.P)); //Ctrl+Shift+P
keys.waitForHotkey(5, "Ctrl+Win+K"); //exception after 5 s
if(!keys.waitForHotkey(-5, "Left")) print.it("timeout"); //returns false after 5 s
```