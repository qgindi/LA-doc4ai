# Method `Au.wpfBuilder.Child`

Sets option for the next `Add` call to add the element as a child or content of the last added element (`Au.wpfBuilder.Last`), which must be a `System.Windows.Controls.Decorator` (for example `System.Windows.Controls.Border` or `System.Windows.Documents.AdornerDecorator`) or `System.Windows.Controls.ContentControl` (for example `System.Windows.Controls.Button`). Also will not change the `Margin` property.

```
public wpfBuilder Child()
```

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    The last added element is not of a supported type.

#### Remarks

Also applies to functions that call `Add`, for example `AddButton`. Does not affect the obsolete hidden `Add` overloads with parameter *flags*.

#### Examples

```
b.R.Add<Border>().Border(Brushes.Green).Child().Add(out TextBlock t1, "Text").Margin("L3R3");
```