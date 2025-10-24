# Method `Au.Types.Coord.Fraction`

Creates `Au.Types.Coord` of `Fraction` type. Value 0 is the left or top of the rectangle. Value 1.0 is the right or bottom of the rectangle. Values \<0 and >=1.0 are outside of the rectangle.

```
public static Coord Fraction(double v)
```

##### Parameters

- *v*  (`double`)

##### Returns

`Au.Types.Coord`

#### Remarks

Instead can be used implicit conversion from `float`, for example argument `Coord.Fraction(.5)` can be replaced with `.5f`.