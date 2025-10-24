# Method `Au.wpfBuilder.Wrap`

## Overload 1

Sets `TextWrapping` property of the last added element. Supports `System.Windows.Controls.TextBlock`, `System.Windows.Controls.TextBox` and `System.Windows.Controls.AccessText`.

```
public wpfBuilder Wrap(TextWrapping wrapping)
```

##### Parameters

- *wrapping*  (`TextWrapping`)

##### Returns

`Au.wpfBuilder`

* * *

## Overload 2

Sets `TextWrapping` property of the last added element = `System.Windows.TextWrapping.Wrap` if `true` (default), else or `System.Windows.TextWrapping.NoWrap`. Supports `System.Windows.Controls.TextBlock`, `System.Windows.Controls.TextBox` and `System.Windows.Controls.AccessText`.

```
public wpfBuilder Wrap(bool wrap = true)
```

##### Parameters

- *wrap*  (`bool`)

##### Returns

`Au.wpfBuilder`