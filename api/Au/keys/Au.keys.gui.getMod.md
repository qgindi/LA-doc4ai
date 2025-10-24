# Method `Au.keys.gui.getMod`

Gets flags indicating which modifier keys are pressed.

```
public static KMod getMod(KMod mod = KMod.Shift | KMod.Ctrl | KMod.Alt)
```

##### Parameters

- *mod*  (`Au.Types.KMod`):
    Check only these keys. Default: `Ctrl`, `Shift`, `Alt`.

##### Returns

`Au.Types.KMod`

#### Remarks

By default does not check the `Win` key, as it is not used in UI, but you can include it in *mod* if need.