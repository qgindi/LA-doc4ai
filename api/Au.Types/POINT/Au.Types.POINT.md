# Struct `Au.Types.POINT`

Point coordinates x y.

```
public record struct POINT : IEquatable<POINT>
```

### Constructors

`POINT(int, int)`

### Fields

`x`, `y`

### Methods

`Deconstruct`, `From`, `From`, `Offset`, `ToString`

### Operators

`operator +(POINT, (int x, int y))`, `implicit operator Point(POINT)`, `implicit operator PointF(POINT)`, `implicit operator Point(POINT)`, `implicit operator POINT(Point)`, `implicit operator POINT((int x, int y))`