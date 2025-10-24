# Struct `Au.Types.Coord`

Contains x or y coordinate in screen or some other rectangle that can be specified in various ways: normal, reverse, fraction, center, max. Used for parameters of functions like `Au.mouse.move`, `Au.wnd.Move`.

```
public record struct Coord : IEquatable<Coord>
```

##### Remarks

To specify a normal coordinate (the origin is the left or top edge), assign an `int` value (implicit conversion from `int` to `Coord`). To specify a reverse coordinate (the origin is the right or bottom edge), use `Au.Types.Coord.Reverse` or a "from end" index like `^1`. It is towards the left or top edge, unless negative. Or use `Au.Types.Coord.Max` or `Au.Types.Coord.MaxInside`. To specify a "fraction of the rectangle" coordinate, use `Au.Types.Coord.Fraction` or a value of type float like `.5f`. Or use `Au.Types.Coord.Center`. The meaning of `default(Coord)` depends on function where used. Many functions interpret it as center (same as `Coord.Center` or `.5f`). Also there are functions to convert `Coord` to normal coordinates.

##### Examples

```
mouse.move(100, 100); //left edge + 100, top edge + 100
mouse.move(Coord.Reverse(100), 100); //right edge - 100, top edge + 100
mouse.move(100, ^100); //left edge + 100, bottom edge - 100
mouse.move(Coord.Fraction(.33), .9f); //left edge + 1/3 of the screen rectangle, top edge + 9/10
mouse.move(Coord.Center, Coord.MaxInside); //x in center (left edge + 1/2), y by the bottom edge inside (Coord.Max would be outside)
mouse.move(Coord.Reverse(-100), 1.1f); //right edge + 100, bottom edge + 0.1 of the rectangle

var w = wnd.find(1, "Untitled - Notepad", "Notepad");
w.Move(.5f, 100, .5f, ^200); //x = center, y = 100, width = half of screen, height = screen height - 200
```

### Properties

`Center`, `FractionValue`, `IsEmpty`, `Max`, `MaxInside`, `Type`, `Value`

### Methods

`Fraction`, `Normalize`, `NormalizeInRange`, `NormalizeInRect`, `NormalizeInWindow`, `Reverse`, `ToString`

### Operators

`implicit operator Coord(Index)`, `implicit operator Coord(int)`, `implicit operator Coord(float)`