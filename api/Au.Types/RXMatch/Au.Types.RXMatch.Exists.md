# Property `Au.Types.RXMatch.Exists`

Gets the return value of the `Au.regexp.Match` call.

```
public bool Exists { get; }
```

##### Property Value

`bool`

#### Remarks

Can be `false` only when the function returned `false` but a mark is available (see `Au.Types.RXMatch.Mark`). Otherwise, when the function returns `false`, it returns `null` instead of a `Au.Types.RXMatch` object. When `false`, all properties except `Au.Types.RXMatch.Exists` and `Au.Types.RXMatch.Mark` have undefined values or throw exception.