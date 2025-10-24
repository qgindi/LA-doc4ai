# Method `Au.keys.more.sendKey`

Sends single key.

```
public static void sendKey(KKey k, bool? down = null, nint hkl = 0, int? extra = null, bool dontThrow = false)
```

##### Parameters

- *k*  (`Au.Types.KKey`):
    Virtual-key code.
- *down*  (`bool?`):
    `true` down, `false` up, `null` down and up.
- *hkl*  (`nint`):
    Keyboard layout handle for scan code. See API `GetKeyboardLayout`. If 0 (default), uses keyboard layout of this thread; don't use 0 for keys whose scancode depends on keyboard layout. If -1, uses keyboard layout of the focused or active window.
- *extra*  (`int?`):
    An "extra info" value that can be used for example by keyboard hooks to recognize the key sender. If `null` (default), uses the same value as other functions of this library.
- *dontThrow*  (`bool`):
    Don't throw exception.

##### Exceptions

- `Au.Types.InputDesktopException`

#### Remarks

This is a low-level function. Does nothing more (sleep, block input, etc). Does not use `Au.opt` options. Just gets missing info (scan code etc) and calls API `SendInput`.