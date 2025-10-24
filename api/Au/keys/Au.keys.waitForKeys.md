# Method `Au.keys.waitForKeys`

Waits for keyboard events using callback function.

```
public static KKey waitForKeys(Seconds timeout, Func<HookData.Keyboard, bool> f, bool block = false)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *f*  (`Func<Au.Types.HookData.Au.Types.HookData.Keyboard, bool>`):
    Callback function that receives key down and up events. Let it return `true` to stop waiting.
- *block*  (`bool`):
    Make the key down event invisible to other apps (when the callback function returns `true`).

##### Returns

`Au.Types.KKey`

Returns the key code. On timeout returns 0 if *timeout* is negative; else exception. For modifier keys returns the left or right key code, for example `LCtrl`/`RCtrl`, not `Ctrl`.

#### Remarks

Waits for key event, not for key state. Uses low-level keyboard hook. Ignores key events injected by functions of this library.

#### Examples

Wait for `F3` or `Esc`.

```
var k = keys.waitForKeys(0, k => !k.IsUp && k.Key is KKey.F3 or KKey.Escape, block: true);
print.it(k);
```