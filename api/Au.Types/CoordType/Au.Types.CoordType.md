# Enum `Au.Types.CoordType`

`Au.Types.Coord` variable value type.

```
public enum CoordType
```

### Fields

| Name | Description |
| --- | --- |
| Fraction | `Au.Types.Coord.FractionValue` is fraction of a rectangle, where 0.0 is left or top, and 1.0 is right or bottom (outside of the rectangle). |
| None | No value. The variable is `default(Coord)`. |
| Normal | `Au.Types.Coord.Value` is pixel offset from left or top of a rectangle. |
| Reverse | `Au.Types.Coord.Value` is pixel offset from right or bottom of a rectangle, towards left or top. |