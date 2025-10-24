# Struct `Au.Types.Strings`

Used for function parameters to specify multiple strings. Contains a string like `"One|Two|Three"` or `string[]` or `List<string>`. Has implicit conversions from these types. Can be assigned collection initializer like `["a", "b"]`.

```
public struct Strings : IEnumerable<string>
```

### Constructors

`Strings(params string[])`

### Properties

`Value`

### Methods

`Create`, `ToArray`

### Operators

`implicit operator Strings(List<string>)`, `implicit operator Strings(string)`, `implicit operator Strings(string[])`