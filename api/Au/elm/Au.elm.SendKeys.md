# Method `Au.elm.SendKeys`

Makes this UI element focused (`Au.elm.Focus`) and calls `Au.keys.send`.

```
public void SendKeys(params KKeysEtc[] keysEtc)
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

- `Exception`:
    Exceptions of `Au.elm.Focus` and `Au.keys.send`.