# Method `Au.keys.getMod`

Gets flags indicating which modifier keys are pressed: `Ctrl`, `Shift`, `Alt`, `Win`. Calls `Au.keys.isPressed`. In UI code use `Au.keys.gui` instead.

```
public static KMod getMod(KMod mod = KMod.Shift | KMod.Ctrl | KMod.Alt | KMod.Win)
```

##### Parameters

- *mod*  (`Au.Types.KMod`):
    Check only these keys. Default - all four.

##### Returns

`Au.Types.KMod`