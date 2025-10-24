# Struct `Au.Types.SIZE`

Width and height.

```
public record struct SIZE : IEquatable<SIZE>
```

### Constructors

`SIZE(int, int)`

### Fields

`height`, `width`

### Methods

`Deconstruct`, `From`, `From`, `ToString`

### Operators

`operator +(SIZE, (int x, int y))`, `implicit operator Size(SIZE)`, `implicit operator SizeF(SIZE)`, `implicit operator Size(SIZE)`, `implicit operator SIZE(Size)`, `implicit operator SIZE((int width, int height))`