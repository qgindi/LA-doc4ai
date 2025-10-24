# Method `Au.keys.gui.isMod`

Returns `true` if some modifier keys are pressed.

```
public static bool isMod(KMod mod = KMod.Shift | KMod.Ctrl | KMod.Alt)
```

##### Parameters

- *mod*  (`Au.Types.KMod`):
    Return `true` if some of these keys are pressed. Default: `Ctrl`, `Shift` or `Alt`.

##### Returns

`bool`

#### Remarks

By default does not check the `Win` key, as it is not used in UI, but you can include it in *mod* if need.