# Method `Au.keys.waitForHotkeys`

Sets a temporary keyboard hook and waits for a hotkey.

```
public static int waitForHotkeys(Seconds timeout, KHotkey[] hotkeys, bool block = true, bool waitModReleased = false)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *hotkeys*  (`Au.Types.KHotkey[]`):
    One or more hotkeys. Examples: `["Ctrl+M"]`, `["Win+M", "Ctrl+Shift+Left"]`.
- *block*  (`bool`):
    Make the key down event of the non-modifier key invisible to other apps. Default `true`.
- *waitModReleased*  (`bool`):
    Also wait until hotkey modifier keys released.

##### Returns

`int`

1-based index of the element in the array of hotkeys. On timeout returns 0 (if *timeout* negative; else exception).

##### Exceptions

- `TimeoutException`

#### Remarks

Uses `Au.keys.waitForKeys`. Works even if the hotkey is used by Windows (except `Win+L` and `Ctrl+Alt+Del`) or an app as a hotkey or trigger.

> **Note:**
> Does not work when the active window has higher UAC integrity level than this process.

#### Examples

```
int i = keys.waitForHotkeys(-10, ["Win+Left", "Win+Right"]);
print.it(i);
```