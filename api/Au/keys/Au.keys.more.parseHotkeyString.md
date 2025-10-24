# Method `Au.keys.more.parseHotkeyString`

## Overload 1

Converts hotkey string like `"Ctrl+A"` to `Au.Types.KKey` and `Au.Types.KMod`.

```
public static bool parseHotkeyString(string s, out KMod mod, out KKey key)
```

##### Parameters

- *s*  (`string`)
- *mod*  (`Au.Types.KMod`)
- *key*  (`Au.Types.KKey`)

##### Returns

`bool`

`false` if the string is invalid.

#### Remarks

For example, if *s* is `"Ctrl+Left"`, sets `mod = KMod.Ctrl`, `key = KKey.Left`.

[Key names](../articles/Key%20names%20and%20operators.html) are like with `Au.keys.send`.

Must be single non-modifier key, preceded by zero or more of modifier keys `Ctrl`, `Shift`, `Alt`, `Win`, all joined with `+`. Valid hotkey examples: `"A"`, `"a"`, `"7"`, `"F12"`, `"."`, `"End"`, `"Ctrl+D"`, `"Ctrl+Alt+Shift+Win+Left"`, `" Ctrl + U "`. Invalid hotkey examples: `null`, `""`, `"A+B"`, `"Ctrl+A+K"`, `"A+Ctrl"`, `"Ctrl+Shift"`, `"Ctrl+"`, `"NoSuchKey"`, `"tab"`.

* * *

## Overload 2

Converts hotkey string like `"Ctrl+A"` to winforms `System.Windows.Forms.Keys`.

```
public static bool parseHotkeyString(string s, out Keys hotkey)
```

##### Parameters

- *s*  (`string`)
- *hotkey*  (`Keys`)

##### Returns

`bool`

`false` if the string is invalid or contains `"Win"`.

#### Remarks

For example, if *s* is `"Ctrl+Left"`, sets `hotkey = Keys.Control | Keys.Left`.

* * *

## Overload 3

Converts hotkey string like `"Ctrl+A"` to WPF `System.Windows.Input.ModifierKeys` and `System.Windows.Input.Key` or `System.Windows.Input.MouseAction`.

```
public static bool parseHotkeyString(string s, out ModifierKeys mod, out Key key, out MouseAction mouse)
```

##### Parameters

- *s*  (`string`)
- *mod*  (`ModifierKeys`)
- *key*  (`Key`)
- *mouse*  (`MouseAction`)

##### Returns

`bool`

`false` if the string is invalid or contains incorrectly specified mouse buttons.

#### Remarks

For example, if *s* is `"Ctrl+Left"`, sets `mod = ModifierKeys.Control` and `key = Key.Left`.

Supported mouse button strings: `"Click"`, `"D-click"`, `"R-click"`, `"M-click"`, `"Wheel"`. Example: `"Ctrl+R-click"`. The first character of a mouse word is case-insensitive.