# Method `Au.wpfBuilder.Row`

Starts new row in current grid.

```
public wpfBuilder Row(WBGridLength height)
```

##### Parameters

- *height*  (`Au.Types.WBGridLength`):

    Row height. Can be:

    - `int` or `double` - `System.Windows.Controls.RowDefinition.Height`. Value 0 means auto-size. Negative value is star-width, ie fraction of total height of star-sized rows. Examples: `50`, `-0.5`.
    - `System.Range` - `System.Windows.Controls.RowDefinition.MinHeight` and/or `System.Windows.Controls.RowDefinition.MaxHeight`. Sets height value = -1 (star-sized). Examples: `50..150`, `50..` or `..150`.
    - tuple `(double value, Range minMax)` - height and min/max heights. Example: `(-2, 50..200)`.
    - `System.Windows.Controls.RowDefinition`.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `InvalidOperationException`:
    In non-grid panel.

#### Remarks

Calling this function is optional, except when not all cells of previous row are explicitly filled.

If there are star-sized rows, grid height should be defined. Call `Au.wpfBuilder.Height` or `Au.wpfBuilder.Size`. But if the grid is in a cell of another grid, usually it's better to set row height of that grid to a non-zero value, ie let it be not auto-sized.