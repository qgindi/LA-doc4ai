# Struct `Au.Types.FolderPath`

Most functions of `Au.folders` class return a value of this type. Contains folder path (string) and has operator `+` to append a string with backslash if need. Has implicit conversions from/to string.

```
public struct FolderPath
```

### Constructors

`FolderPath(string)`

### Properties

`IsNull`, `Path`, `PathOrThrow`

### Methods

`ToString`

### Operators

`operator +(FolderPath, string)`, `explicit operator FolderPath(string)`, `implicit operator string(FolderPath)`