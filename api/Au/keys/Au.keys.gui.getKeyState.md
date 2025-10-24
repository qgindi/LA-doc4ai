# Method `Au.keys.gui.getKeyState`

Calls API `GetKeyState` and returns its return value.

```
public static short getKeyState(KKey key)
```

##### Parameters

- *key*  (`Au.Types.KKey`)

##### Returns

`short`

#### Remarks

If returns \< 0, the key is pressed. If the low-order bit is 1, the key is toggled; it works only with `CapsLock`, `NumLock`, `ScrollLock` and several other keys, as well as mouse buttons. Can be used for mouse buttons too, for example `keys.gui.getKeyState(KKey.MouseLeft)`. When mouse left and right buttons are swapped, gets logical state, not physical.