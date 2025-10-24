# Method `Au.keys.AddKey`

## Overload 1

Adds single key, specified as `Au.Types.KKey`, to the internal collection. It will be sent by `Au.keys.SendNow`.

```
public keys AddKey(KKey key, bool? down = null)
```

##### Parameters

- *key*  (`Au.Types.KKey`):
    Virtual-key code, like `KKey.Tab` or `(KKey)200`. Valid values are 1-255.
- *down*  (`bool?`):
    `true` - key down; `false` - key up; `null` (default) - key down-up.

##### Returns

`Au.keys`

This.

##### Exceptions

- `ArgumentException`:
    Invalid *key* (0).

* * *

## Overload 2

Adds single key to the internal collection. Allows to specify scan code and whether it is an extended key. It will be sent by `Au.keys.SendNow`.

```
public keys AddKey(KKey key, ushort scanCode, bool extendedKey, bool? down = null)
```

##### Parameters

- *key*  (`Au.Types.KKey`):
    Virtual-key code, like `KKey.Tab` or `(KKey)200`. Valid values are 1-255. Can be 0.
- *scanCode*  (`ushort`):
    Scan code of the physical key. Scan code values are 1-127, but this function allows 1-0xffff. Can be 0.
- *extendedKey*  (`bool`):
    `true` if the key is an extended key.
- *down*  (`bool?`):
    `true` - key down; `false` - key up; `null` (default) - key down-up.

##### Returns

`Au.keys`

This.

##### Exceptions

- `ArgumentException`:
    Invalid scan code.