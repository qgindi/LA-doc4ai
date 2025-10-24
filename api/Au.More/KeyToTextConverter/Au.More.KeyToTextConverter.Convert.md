# Method `Au.More.KeyToTextConverter.Convert`

Converts a virtual-key code to text.

```
public bool Convert(out (char c, string s) text, KKey vk, uint sc, KMod mod, int threadId)
```

##### Parameters

- *text*  (`(char c, string s)`):
    Receives text. Can be 1 character *c*, or string *s* with 2 or more characters. Receives default if this function returns `false` or if the key is a dead key.
- *vk*  (`Au.Types.KKey`):
    Virtual-key code.
- *sc*  (`uint`):
    Scan code.
- *mod*  (`Au.Types.KMod`):
    Modifier keys (`Shift` etc). See `Au.keys.getMod`.
- *threadId*  (`int`):
    Thread id of the focused or active window. Need for keyboard layout. If 0, uses this thread.

##### Returns

`bool`

`true` if it's a text key or dead key.