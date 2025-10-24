# Property `Au.Triggers.AutotextTriggerArgs.ShiftLeft`

If `true`, `Au.Triggers.AutotextTriggerArgs.Replace` will select text with `Shift+Left` instead of erasing with `Backspace`. Except in console windows.

```
public bool ShiftLeft { get; set; }
```

##### Property Value

`bool`

#### Remarks

Initially `true` if flag `Au.Triggers.TAFlags.ShiftLeft` is set. Can be changed by a callback function, for example to use or not use `Shift+Left` only with some windows.