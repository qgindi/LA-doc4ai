# Method `Au.keys.sendL`

Generates virtual keystrokes. Like `Au.keys.send`, but without reliability features: delays, user input blocking, resetting modifiers/`CapsLock`.

```
public static void sendL(params KKeysEtc[] keysEtc)
```

##### Parameters

- *keysEtc*  (`Au.Types.KKeysEtc[]`):

    Arguments of these types:

    - string - [key names and operators](../articles/Key%20names%20and%20operators.html), like `"Enter A Ctrl+A"`.
 Tool: in `""` string press `Ctrl+Space`.
    - string with prefix `"!"` - literal text.
 Example: `var p = "pass"; keys.send("!user", "Tab", "!" + p, "Enter");`
    - string with prefix `"%"` - HTML to paste. Full or fragment.
    - `Au.clipboardData` - clipboard data to paste.
    - `Au.Types.KKey` - a single key.
 Example: `keys.send("Shift+", KKey.Left, "*3");` is the same as `keys.send("Shift+Left*3");`
    - `int` - sleep milliseconds. Max 10000.
 Example: `keys.send("Left", 500, "Right");`
    - `System.Action` - callback function.
 Example: `Action click = () => mouse.click(); keys.send("Shift+", click);`
    - `Au.Types.KKeyScan` - a single key, specified using scan code and/or virtual-key code and extended-key flag.
 Example: `keys.send(new KKeyScan(0x3B, false)); //key F1`
 Example: `keys.send(new KKeyScan(KKey.Enter, true)); //numpad Enter`
    - `char` - a single character. Like text with `Au.Types.OKeyText.KeysOrChar` or operator `^`.

##### Exceptions

- `ArgumentException`:
    An invalid value, for example an unknown key name.
- `Au.Types.AuException`:
    Failed. When sending text, fails if there is no focused window.
- `Au.Types.InputDesktopException`

#### Remarks

Ignores `Au.opt.key` and instead uses default options with these changes:

- `SleepFinally` = 0.
- `KeySpeed` = 0.
- `NoBlockInput` = `true`.
- `NoCapsOff` = `true`.
- `NoModOff` = `true`.

### See Also

`Au.keys.more.sendKey`