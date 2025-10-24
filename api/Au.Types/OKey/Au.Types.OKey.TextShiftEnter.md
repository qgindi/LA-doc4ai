# Property `Au.Types.OKey.TextShiftEnter`

When sending text, instead of `Enter` send `Shift+Enter`. Default: false.

```
public bool TextShiftEnter { get; set; }
```

##### Property Value

`bool`

#### Remarks

This option is applied when sending text with `Au.keys.sendt` (like `keys.sendt("A\nB")`) or with operator `!` (like `keys.send("!A\nB")`) or with `Au.keys.AddText`. Ignored when using operator `^`, `_`, `Au.keys.AddText`, `Au.keys.AddChar`.