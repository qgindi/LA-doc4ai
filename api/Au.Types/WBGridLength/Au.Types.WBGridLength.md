# Struct `Au.Types.WBGridLength`

Used with `Au.wpfBuilder` functions to specify width/height of columns and rows. Allows to specify minimal and/or maximal values too.

```
public struct WBGridLength
```

##### Remarks

Like `Au.Types.WBLength`, but has functions to create `System.Windows.Controls.ColumnDefinition` and `System.Windows.Controls.RowDefinition`. Also has implicit conversion from these types.

### Properties

`Column`, `Row`

### Operators

`implicit operator WBGridLength(double)`, `implicit operator WBGridLength(Range)`, `implicit operator WBGridLength((double length, Range minMax))`, `implicit operator WBGridLength(DefinitionBase)`