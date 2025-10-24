# Method `Au.wpfBuilder.Select`

## Overload 1

Selects an item of the last added `System.Windows.Controls.Primitives.Selector` (`System.Windows.Controls.ComboBox`, etc).

```
public wpfBuilder Select(int index)
```

##### Parameters

- *index*  (`int`):
    0-based item index

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    The last added element is not `System.Windows.Controls.Primitives.Selector`.

### See Also

`Au.wpfBuilder.Items`

* * *

## Overload 2

Selects an item of the last added `System.Windows.Controls.Primitives.Selector` (`System.Windows.Controls.ComboBox`, etc).

```
public wpfBuilder Select(object item)
```

##### Parameters

- *item*  (`object`):
    An added item.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    The last added element is not `System.Windows.Controls.Primitives.Selector`.

### See Also

`Au.wpfBuilder.Items`