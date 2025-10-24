# Struct `Au.Types.RECT`

Rectangle coordinates left top right bottom.

```
public record struct RECT : IEquatable<RECT>
```

##### Remarks

This type can be used with Windows API functions. The .NET `Rectangle` etc can't, because their fields are different. Has conversions from/to `System.Drawing.Rectangle`.

### Constructors

`RECT(int, int, int, int)`

### Fields

`bottom`, `left`, `right`, `top`

### Properties

`CenterX`, `CenterY`, `Height`, `Is0`, `NoArea`, `Size`, `Width`, `XY`

### Methods

`Contains`, `Contains`, `Contains`, `EnsureInScreen`, `From`, `From`, `FromLTRB`, `Inflate`, `Intersect`, `Intersect`, `IntersectsWith`, `Move`, `MoveInRect`, `MoveInScreen`, `Normalize`, `Offset`, `ToString`, `ToStringFormat`, `ToStringSimple`, `TryParse`, `Union`, `Union`

### Operators

`implicit operator Rectangle(RECT)`, `implicit operator RectangleF(RECT)`, `implicit operator Rect(RECT)`, `implicit operator RECT(Rectangle)`, `implicit operator RECT((int L, int T, int W, int H))`