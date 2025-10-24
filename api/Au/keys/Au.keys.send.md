# Method `Au.keys.send`

Generates virtual keystrokes (keys, text).

```
public static void send(params KKeysEtc[] keysEtc)
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

String syntax: [key names and operators](../articles/Key%20names%20and%20operators.html).

Uses `Au.opt.key`:

| Option | Default | Changed |
| --- | --- | --- |
| `Au.Types.OKey.NoBlockInput` | `false`. Blocks user-pressed keys. Sends them afterwards. <br>If the last argument is "sleep", stops blocking before executing it; else stops blocking after executing all arguments. | `true`. Does not block user-pressed keys. |
| `Au.Types.OKey.NoCapsOff` | `false`. If the `CapsLock` key is toggled, untoggles it temporarily (presses it before and after). | `true`. Does not touch the `CapsLock` key. <br>Alphabetic keys of "keys" arguments can depend on `CapsLock`. Text of "text" arguments doesn't depend on `CapsLock`, unless `Au.Types.OKey.TextHow` is `KeysX`. |
| `Au.Types.OKey.NoModOff` | `false`. Releases modifier keys (`Alt`, `Ctrl`, `Shift`, `Win`). <br>Does it only at the start; later they cannot interfere, unless `Au.Types.OKey.NoBlockInput` is `true`. | `true`. Does not touch modifier keys. |
| `Au.Types.OKey.TextSpeed` | 0 ms. | 0 - 1000. Changes the speed for "text" arguments. |
| `Au.Types.OKey.KeySpeed` | 2 ms. | 0 - 1000. Changes the speed for "keys" arguments. |
| `Au.Types.OKey.KeySpeedClipboard` | 5 ms. | 0 - 1000. Changes the speed of `Ctrl+V` keys when pasting text or HTML using clipboard. |
| `Au.Types.OKey.SleepFinally` | 10 ms. | 0 - 10000. <br>Tip: to sleep finally, also can be used code like this: `keys.send("keys", 1000);`. |
| `Au.Types.OKey.TextHow` | `Au.Types.OKeyText.Characters`. | `KeysOrChar`, `KeysOrPaste` or `Paste`. |
| `Au.Types.OKey.TextShiftEnter` | `false`. | `true`. When sending text, instead of `Enter` send `Shift+Enter`. |
| `Au.Types.OKey.PasteLength` | 200. <br>This option is used for "text" arguments. If text length >= this value, uses clipboard. | >=0. |
| `Au.Types.OKey.PasteWorkaround` | `false`. <br>This option is used for "text" arguments when using clipboard. | `true`. |
| `Au.Types.OKey.RestoreClipboard` | `true`. Restore clipboard data (by default only text). <br>This option is used for "text" and "HTML" arguments when using clipboard. | `false`. Don't restore clipboard data. |
| `Au.Types.OKey.Hook` | `null`. | Callback function that can modify options depending on active window etc. |

This function does not wait until the target app receives and processes sent keystrokes and text; there is no reliable way to know it. It just adds small delays depending on options (`Au.Types.OKey.SleepFinally` etc). If need, change options or add "sleep" arguments or wait after calling this function. Sending text through the clipboard normally does not have these problems.

Don't use this function to automate windows of own thread. Call it from another thread. See example with async/await.

Administrator and uiAccess processes don't receive keystrokes sent by standard user processes. See [UAC](../articles/UAC.html).

Mouse button codes/names (eg `Au.Types.KKey.MouseLeft`) cannot be used to click. Instead use callback, like in the "Ctrl+click" example.

You can use a `Au.keys` variable instead of this function. Example: `new keys(null).Add("keys", "!text").SendNow();`. More examples in `Au.keys.keys` topic.

This function calls `Au.keys.Add`, which calls these functions depending on argument type: `Au.keys.AddKeys`, `Au.keys.AddText`, `Au.keys.AddChar`, `Au.keys.AddClipboardData`, `Au.keys.AddKey`, `Au.keys.AddKey`, `Au.keys.AddSleep`, `Au.keys.AddAction`. Then calls `Au.keys.SendNow`.

Uses API `SendInput`.

#### Examples

```
//Press key Enter.
keys.send("Enter");

//Press keys Ctrl+A.
keys.send("Ctrl+A");

//Ctrl+Alt+Shift+Win+A.
keys.send("Ctrl+Alt+Shift+Win+A");

//Alt down, E, P, Alt up.
keys.send("Alt+(E P)");

//Alt down, E, P, Alt up.
keys.send("Alt*down E P Alt*up");

//Send text "Example".
keys.send("!Example");
keys.sendt("Example"); //same

//Press key End, key Backspace 3 times, send text "Text".
keys.send("End Back*3", "!Text");

//Press Tab n times, send text "user", press Tab, send text "password", press Enter.
int n = 5; string pw = "password";
keys.send($"Tab*{n}", "!user", "Tab", "!" + pw, "Enter");

//Press Ctrl+V, wait 500 ms, press Enter.
keys.send("Ctrl+V", 500, "Enter");

//F2, Ctrl+K, Left 3 times, Space, A, comma, 5, numpad 5, BrowserBack.
keys.send("F2 Ctrl+K Left*3 Space a , 5 #5", KKey.BrowserBack);

//Shift down, A 3 times, Shift up.
keys.send("Shift+A*3");

//Shift down, A 3 times, Shift up.
keys.send("Shift+", KKey.A, "*3");

//Shift down, A, wait 500 ms, B, Shift up.
keys.send("Shift+(", KKey.A, 500, KKey.B, ")");

//Send keys and text slowly.
opt.key.KeySpeed = opt.key.TextSpeed = 50;
keys.send("keys Shift+: Space 123456789 Space 123456789 ,Space", "!text: 123456789 123456789\n");

//Ctrl+click
Action click = () => mouse.click();
keys.send("Ctrl+", click);

//Ctrl+click
keys.send("Ctrl+", new Action(() => mouse.click()));
```

Show window and send keys/text to it when button clicked.

```
var b = new wpfBuilder("Window").WinSize(250);
b.R.AddButton("Keys", async _ => {
	//keys.send("Tab", "!text", 2000, "Esc"); //no
	await Task.Run(() => { keys.send("Tab", "!text", 2000, "Esc"); }); //use other thread
});
b.R.Add("Text", out TextBox text1);
b.R.AddOkCancel();
b.End();
if (!b.ShowDialog()) return;
```