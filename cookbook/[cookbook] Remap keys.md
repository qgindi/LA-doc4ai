# Remap keys

There are 3 ways to remap keyboard keys or characters:

1. Use [keyboard triggers](Keyboard%20triggers%20%28hotkeys%29.html). It is the most flexible way. Less reliable, for example may not work in some windows.
2. Modify the Registry. It remaps keys. Look for software that can do it.
3. Create and install a custom keyboard layout. It remaps characters. Use Microsoft Keyboard Layout Creator or similar software.

The rest of this recipe is about the first way (keyboard triggers). Assume the codes are in file `Hotkey triggers`. Note: to remap keys use `keys.more.sendKey` or `keys.sendL`, not `keys.send`.

```
using Au.Triggers;
```

Disable key `CapsLock` when pressed without modifiers (`Ctrl` etc).

```
hk["CapsLock"] = o => {  };
```

Remap key `Insert` to `Apps`. With `?+` also remaps `Ctrl+Insert` etc.

```
hk["?+Ins"] = o => keys.more.sendKey(KKey.Apps);
```

Remap numeric keypad keys to characters when `NumLock` inactive. Lowercase or uppercase, depending on `Shift` and `CapsLock`.

```
var flags1 = TKFlags.ExtendedNo | TKFlags.NoModOff;
hk["Shift?+Home", flags1] = o => _RemapToChar(o, 'ą'); // 1
hk["Shift?+Up", flags1] = o => _RemapToChar(o, 'č'); // 2
hk["Shift?+PgUp", flags1] = o => _RemapToChar(o, 'ę'); // 3
hk["Shift?+Left", flags1] = o => _RemapToChar(o, 'ė'); // 4
hk["Shift?+Clear", flags1] = o => _RemapToChar(o, 'į'); // 5
hk["Shift?+Right", flags1] = o => _RemapToChar(o, 'š'); // 6
hk["Shift?+End", flags1] = o => _RemapToChar(o, 'ų'); // 7
hk["Shift?+Down", flags1] = o => _RemapToChar(o, 'ū'); // 8
hk["Shift?+PgDn", flags1] = o => _RemapToChar(o, 'ž'); // 9

void _RemapToChar(HotkeyTriggerArgs o, char c) {
	bool upper = o.Mod.Has(KMod.Shift);
	if (keys.isCapsLock) upper ^= true;
	if (upper) c = char.ToUpperInvariant(c);
	keys.sendL(c);
}
```