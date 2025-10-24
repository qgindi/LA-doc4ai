# Struct `Au.Types.StartEnd`

Struct with fields `int start` and `int end`.

```
public record struct StartEnd : IEquatable<StartEnd>
```

### Constructors

`StartEnd(int, int)`

### Fields

`end`, `start`

### Properties

`Length`, `Range`

### Methods

`ToString`

### Operators

`implicit operator Range(StartEnd)`, `implicit operator StartEnd(Range)`