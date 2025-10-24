# Method `Au.wpfBuilder.Image`

## Overload 1

Loads image into the last added `System.Windows.Controls.Image`.

```
public wpfBuilder Image(ImageSource source, Stretch stretch = Stretch.None, StretchDirection stretchDirection = StretchDirection.DownOnly)
```

##### Parameters

- *source*  (`ImageSource`):
    Sets `System.Windows.Controls.Image.Source`.
- *stretch*  (`Stretch`):
    Sets `System.Windows.Controls.Image.Stretch`.
- *stretchDirection*  (`StretchDirection`):
    Sets `System.Windows.Controls.Image.StretchDirection`.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    The last added element is not `System.Windows.Controls.Image`.

#### Remarks

To load vector images from XAML, don't use `System.Windows.Controls.Image` control and this function. Instead create control from XAML, for example with `Au.More.ImageUtil.LoadWpfImageElement`, and add it with `Au.wpfBuilder.Add`.

### See Also

`Au.icon.ToWpfImage`

`Au.More.ImageUtil`

* * *

## Overload 2

Loads image from a file or URL into the last added `System.Windows.Controls.Image`.

```
public wpfBuilder Image(string source, Stretch stretch = Stretch.None, StretchDirection stretchDirection = StretchDirection.DownOnly)
```

##### Parameters

- *source*  (`string`):
    File path etc. See `Au.More.ImageUtil.LoadWpfImage`. Sets `System.Windows.Controls.Image.Source`.
- *stretch*  (`Stretch`):
    Sets `System.Windows.Controls.Image.Stretch`.
- *stretchDirection*  (`StretchDirection`):
    Sets `System.Windows.Controls.Image.StretchDirection`.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    The last added element is not `System.Windows.Controls.Image`.

#### Remarks

If fails to load, prints warning. See `Au.print.warning`.