# Method `Au.keys.gui.isPressed`

Returns `true` if the specified key or mouse button is pressed.

```
public static bool isPressed(KKey key)
```

##### Parameters

- *key*  (`Au.Types.KKey`)

##### Returns

`bool`

#### Remarks

Can be used for mouse buttons too. Example: `keys.gui.isPressed(KKey.MouseLeft)`. When mouse left and right buttons are swapped, gets logical state, not physical.