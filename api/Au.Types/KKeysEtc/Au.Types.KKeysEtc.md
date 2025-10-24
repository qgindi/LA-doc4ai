# Struct `Au.Types.KKeysEtc`

Parameter type of `Au.keys.send` and similar functions. Has implicit conversions from `string`, `Au.clipboardData`, `Au.Types.KKey`, `Au.Types.KKeyScan`, `char`, `int` (sleep time) and `System.Action`.

```
public struct KKeysEtc
```

### Constructors

`KKeysEtc(Action)`

### Properties

`Value`

### Operators

`implicit operator KKeysEtc(KKey)`, `implicit operator KKeysEtc(KKeyScan)`, `implicit operator KKeysEtc(clipboardData)`, `implicit operator KKeysEtc(Action)`, `implicit operator KKeysEtc(char)`, `implicit operator KKeysEtc(int)`, `implicit operator KKeysEtc(string)`