# Method `Au.wpfBuilder.Border`

## Overload 1

Sets border properties of the last added element, which can be `Au.wpfBuilder.Border(Brush, double, Thickness?, double?, Thickness?)` or a `System.Windows.Controls.Control`-derived class.

```
public wpfBuilder Border(Brush color = null, double thickness = 1, Thickness? padding = null, double? cornerRadius = null, Thickness? thickness2 = null)
```

##### Parameters

- *color*  (`Brush`):
    Border color brush. If `null`, uses `System.Windows.SystemColors.ActiveBorderBrush`.
- *thickness*  (`double`):
    Border thickness. Ignored if *thickness2* not `null`.
- *padding*  (`Thickness?`):
    Sets the `Padding` property.
- *cornerRadius*  (`double?`):
    Sets `System.Windows.Controls.Border.CornerRadius`. If used, the last added element must be `System.Windows.Controls.Border`.
- *thickness2*  (`Thickness?`):
    Border thickness to use instead of *thickness*. Allows to set non-uniform thickness.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    Last added element must be `System.Windows.Controls.Control` or `System.Windows.Controls.Border`. With *cornerRadius* only `System.Windows.Controls.Border`.

#### Examples

```
b.R.Add<Label>("Example1").Border(Brushes.BlueViolet, 1, new(5)).Brush(Brushes.Cornsilk, Brushes.Green);
b.R.Add<Border>().Border(Brushes.Blue, 2, cornerRadius: 3).Child().Add<Label>("Example2");
```

* * *

## Overload 2

Sets border properties of the last added element, which can be `Au.wpfBuilder.Border(Brush, double, Thickness?, double?, Thickness?)` or a `System.Windows.Controls.Control`-derived class.

```
public wpfBuilder Border(ColorInt color, double thickness = 1, Thickness? padding = null, double? cornerRadius = null, Thickness? thickness2 = null)
```

##### Parameters

- *color*  (`Au.Types.ColorInt`):
    Border color.
- *thickness*  (`double`):
    Border thickness. Ignored if *thickness2* not `null`.
- *padding*  (`Thickness?`):
    Sets the `Padding` property.
- *cornerRadius*  (`double?`):
    Sets `System.Windows.Controls.Border.CornerRadius`. If used, the last added element must be `System.Windows.Controls.Border`.
- *thickness2*  (`Thickness?`):
    Border thickness to use instead of *thickness*. Allows to set non-uniform thickness.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    Last added element must be `System.Windows.Controls.Control` or `System.Windows.Controls.Border`. With *cornerRadius* only `System.Windows.Controls.Border`.

#### Examples

```
b.R.Add<Label>("Example1").Border(Brushes.BlueViolet, 1, new(5)).Brush(Brushes.Cornsilk, Brushes.Green);
b.R.Add<Border>().Border(Brushes.Blue, 2, cornerRadius: 3).Child().Add<Label>("Example2");
```