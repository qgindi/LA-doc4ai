# Struct `Au.Types.FAttr`

Contains file or directory attributes. Tells whether it exists, is directory, readonly, hidden, system, NTFS link. See `Au.filesystem.exists`.

```
public struct FAttr
```

### Properties

`Attributes`, `Directory`, `Exists`, `File`, `IsHidden`, `IsNtfsLink`, `IsReadonly`, `IsSystem`, `Unknown`

### Methods

`ToString`

### Operators

`implicit operator bool(FAttr)`, `implicit operator int(FAttr)`