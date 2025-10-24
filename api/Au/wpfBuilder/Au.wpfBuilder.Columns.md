# Method `Au.wpfBuilder.Columns`

Sets column count and widths of current grid.

```
public wpfBuilder Columns(params WBGridLength[] widths)
```

##### Parameters

- *widths*  (`Au.Types.WBGridLength[]`):

    Column widths. An argument can be:

    - `int` or `double` - `System.Windows.Controls.ColumnDefinition.Width`. Value 0 means auto-size. Negative value is star-width, ie fraction of total width of star-sized columns. Examples: `50`, `-0.5`.
    - `System.Range` - `System.Windows.Controls.ColumnDefinition.MinWidth` and/or `System.Windows.Controls.ColumnDefinition.MaxWidth`. Sets width value = -1 (star-sized). Examples: `50..150`, `50..` or `..150`.
    - tuple `(double value, Range minMax)` - width and min/max widths. Example: `(-2, 50..)`.
    - `System.Windows.Controls.ColumnDefinition`.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `InvalidOperationException`:
    Columns() in non-grid panel or after an `Add` function.

#### Remarks

If this function not called, the table has 2 columns like `.Columns(0, -1)`.

If there are star-sized columns, should be set width of the grid or of its container. Call `Au.wpfBuilder.Width` or `Au.wpfBuilder.Size` or `Au.wpfBuilder.WinSize`. But if the grid is in a cell of another grid, usually it's better to set column width of that grid to a non-zero value, ie let it be not auto-sized.