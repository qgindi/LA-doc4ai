# Method `Au.wpfBuilder.Checked`

## Overload 1

Sets `System.Windows.Controls.Primitives.ToggleButton.IsChecked` and `System.Windows.Controls.Primitives.ToggleButton.IsThreeState` of the last added check box or radio button.

```
public wpfBuilder Checked(bool? check = true, bool threeState = false)
```

##### Parameters

- *check*  (`bool?`)
- *threeState*  (`bool`)

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    The last added element is not `System.Windows.Controls.Primitives.ToggleButton`.

* * *

## Overload 2

Sets `System.Windows.Controls.Primitives.ToggleButton.IsChecked` of the specified `System.Windows.Controls.RadioButton`.

```
public wpfBuilder Checked(bool check, RadioButton control)
```

##### Parameters

- *check*  (`bool`)
- *control*  (`RadioButton`)

##### Returns

`Au.wpfBuilder`

#### Remarks

Unlike other similar functions, does not use `Au.wpfBuilder.Last`.