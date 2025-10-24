# Property `Au.Types.HookData.Keyboard.Key`

If `Au.Types.HookData.Keyboard.vkCode` is a left or right modifier key code (`LShift`, `LCtrl`, `LAlt`, `RShift`, `RCtrl`, `RAlt`, `RWin`), returns the common modifier key code (`Shift`, `Ctrl`, `Alt`, `Win`). Else returns `Au.Types.HookData.Keyboard.vkCode`.

```
public KKey Key { get; }
```

##### Property Value

`Au.Types.KKey`