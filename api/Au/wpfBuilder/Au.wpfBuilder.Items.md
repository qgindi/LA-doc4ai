# Method `Au.wpfBuilder.Items`

## Overload 1

Splits string and ads substrings as items to the last added `System.Windows.Controls.ItemsControl` (`System.Windows.Controls.ComboBox`, etc).

```
public wpfBuilder Items(string items)
```

##### Parameters

- *items*  (`string`):
    String like `"One|Two|Three"`.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    The last added element is not `System.Windows.Controls.ItemsControl`.

#### Remarks

If it is a non-editable `System.Windows.Controls.ComboBox`, selects the first item. See also `Au.wpfBuilder.Select`.

* * *

## Overload 2

Adds items of any type to the last added `System.Windows.Controls.ItemsControl` (`System.Windows.Controls.ComboBox`, etc).

```
public wpfBuilder Items(params object[] items)
```

##### Parameters

- *items*  (`object[]`):
    Items of any type (`string`, WPF element).

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    The last added element is not `System.Windows.Controls.ItemsControl`.

#### Remarks

If it is a non-editable `System.Windows.Controls.ComboBox`, selects the first item. See also `Au.wpfBuilder.Select`.

* * *

## Overload 3

Adds items as `System.Collections.IEnumerable` to the last added `System.Windows.Controls.ItemsControl` (`System.Windows.Controls.ComboBox`, etc), with "lazy" option.

```
public wpfBuilder Items(IEnumerable items, bool lazy = false)
```

##### Parameters

- *items*  (`IEnumerable`):
    An `System.Collections.IEnumerable` that contains items (eg array, `System.Collections.Generic.List<T>`) or generates items (eg returned from a yield-return function).
- *lazy*  (`bool`):
    Retrieve items when (if) showing the dropdown part of the `System.Windows.Controls.ComboBox` first time.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:

    - The last added element is not `System.Windows.Controls.ItemsControl`.
    - *lazy* is `true` and the last added element is not `System.Windows.Controls.ComboBox`.

* * *

## Overload 4

Sets callback function that should add items to the last added `System.Windows.Controls.ComboBox` later.

```
public wpfBuilder Items(bool once, Action<ComboBox> onDropDown)
```

##### Parameters

- *once*  (`bool`):
    Call the function once. If `false`, calls on each drop down.
- *onDropDown*  (`Action<ComboBox>`):
    Callback function that should add items. Called before showing the dropdown part of the `System.Windows.Controls.ComboBox`. Don't need to clear old items.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    The last added element is not `System.Windows.Controls.ComboBox`.