# Struct `Au.Types.ColorInt`

Color, as `int` in `0xAARRGGBB` format. Can convert from/to `System.Drawing.Color`, `System.Windows.Media.Color`, `int` (`0xAARRGGBB`), Windows `COLORREF` (`0xBBGGRR`), string.

```
public record struct ColorInt : IEquatable<ColorInt>
```

### Constructors

`ColorInt(int, bool?)`, `ColorInt(uint, bool?)`

### Fields

`argb`

### Methods

`FromBGR`, `FromHLS`, `FromString`, `GetPerceivedBrightness`, `SwapRB`, `SwapRB`, `ToBGR`, `ToHLS`, `ToString`

### Operators

`explicit operator Color(ColorInt)`, `explicit operator Color(ColorInt)`, `implicit operator ColorInt(Color)`, `implicit operator ColorInt(int)`, `implicit operator ColorInt(uint)`, `implicit operator ColorInt(Color)`