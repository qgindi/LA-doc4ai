# Method `Au.wpfBuilder.Brush`

## Overload 1

Sets background and/or foreground brush (color, gradient, etc) of the last added element.

```
public wpfBuilder Brush(Brush background = null, Brush foreground = null)
```

##### Parameters

- *background*  (`Brush`):
    Background brush. See `System.Windows.Media.Brushes`, `System.Windows.SystemColors`. Descendants usually inherit this property.
- *foreground*  (`Brush`):
    Foreground brush. Usually sets text color. Descendants usually override this property.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    Last added element must be `System.Windows.Controls.Control`, `Au.wpfBuilder.Panel`, `Au.wpfBuilder.Border` or `System.Windows.Controls.TextBlock`. With *foreground* only `System.Windows.Controls.Control` or `System.Windows.Controls.TextBlock`.

#### Examples

```
b.R.Add<Label>("Example1").Brush(Brushes.Cornsilk, Brushes.Green).Border(Brushes.BlueViolet, 1);
b.R.Add<Label>("Example2").Brush(new LinearGradientBrush(Colors.Chocolate, Colors.White, 0));
```

* * *

## Overload 2

Sets background and/or foreground color of the last added element.

```
public wpfBuilder Brush(ColorInt? background = null, ColorInt? foreground = null)
```

##### Parameters

- *background*  (`Au.Types.ColorInt?`)
- *foreground*  (`Au.Types.ColorInt?`)

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    Last added element must be `System.Windows.Controls.Control`, `Au.wpfBuilder.Panel`, `Au.wpfBuilder.Border` or `System.Windows.Controls.TextBlock`. With *foreground* only `System.Windows.Controls.Control` or `System.Windows.Controls.TextBlock`.