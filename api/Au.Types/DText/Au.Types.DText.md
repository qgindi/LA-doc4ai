# Class `Au.Types.DText`

Text for `Au.dialog` functions. Supports links. Has implicit conversion from string.

```
public record DText : IEquatable<DText>
```

##### Inheritance

`object` → `DText`

### Constructors

`DText(string, params Action<DEventArgs>[])`

### Properties

`text`

### Operators

`implicit operator DText(string)`