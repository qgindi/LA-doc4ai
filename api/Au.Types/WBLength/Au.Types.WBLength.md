# Struct `Au.Types.WBLength`

Used with `Au.wpfBuilder` functions for width/height parameters. Allows to specify minimal and/or maximal values too.

```
public struct WBLength
```

##### Remarks

Has implicit conversions from `double`, `System.Range` and tuple `(double length, Range minMax)`. To specify width or height, pass an `int` or `double` value, like `100` or `15.25`. To specify minimal value, pass a range like `100..`. To specify maximal value, pass a range like `..100`. To specify minimal and maximal values, pass a range like `100..500`. To specify width or height and minimal or/and maximal values, pass a tuple like `(100, 50..)` or `(100, ..200)` or `(100, 50..200)`.

### Methods

`ApplyTo`, `GetLength`, `GetMax`, `GetMin`

### Operators

`implicit operator WBLength(double)`, `implicit operator WBLength(Range)`, `implicit operator WBLength((double length, Range minMax))`