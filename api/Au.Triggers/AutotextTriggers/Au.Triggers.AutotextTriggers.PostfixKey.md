# Property `Au.Triggers.AutotextTriggers.PostfixKey`

The postfix key for all triggers where postfix type is `Au.Triggers.TAPostfix.Key` or `Au.Triggers.TAPostfix.CharOrKey` (default). Can be `Ctrl` (default), `Shift`, `LCtrl`, `RCtrl`, `LShift` or `RShift`.

```
public KKey PostfixKey { get; set; }
```

##### Exceptions

- `ArgumentException`:
    The value is not `Ctrl` or `Shift`.

##### Property Value

`Au.Types.KKey`

#### Remarks

This property is applied to all triggers, not just to those added afterwards.