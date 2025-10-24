# Method `Au.keys.isMod`

Returns `true` if some modifier keys are pressed: `Ctrl`, `Shift`, `Alt`, `Win`. Calls `Au.keys.isPressed`. In UI code use `Au.keys.gui` instead.

```
public static bool isMod(KMod mod = KMod.Shift | KMod.Ctrl | KMod.Alt | KMod.Win)
```

##### Parameters

- *mod*  (`Au.Types.KMod`):
    Return `true` if some of these keys are pressed. Default - any.

##### Returns

`bool`

### See Also

`Au.keys.waitForNoModifierKeys`