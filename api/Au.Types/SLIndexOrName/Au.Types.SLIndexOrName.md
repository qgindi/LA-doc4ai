# Struct `Au.Types.SLIndexOrName`

Used for parameter types of some `Au.sqliteStatement` functions. Has implicit conversions from `int` and `string`. If `int`, the value is interpreted as index. If `string` - as name.

```
public struct SLIndexOrName
```

### Fields

`index`, `name`

### Operators

`implicit operator SLIndexOrName(int)`, `implicit operator SLIndexOrName(string)`