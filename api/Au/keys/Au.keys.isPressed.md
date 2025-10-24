# Method `Au.keys.isPressed`

Returns `true` if the specified key or mouse button is pressed. In UI code use `Au.keys.gui` instead.

```
public static bool isPressed(KKey key)
```

##### Parameters

- *key*  (`Au.Types.KKey`)

##### Returns

`bool`

#### Remarks

Uses API `GetAsyncKeyState`.