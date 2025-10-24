# Method `Au.Types.ExtWpf.AddColumns`

Adds one or more columns. Like `Au.wpfBuilder.Columns`, but does not clear existing columns.

```
public static void AddColumns(this Grid g, params WBGridLength[] widths)
```

##### Parameters

- *g*  (`Grid`)
- *widths*  (`Au.Types.WBGridLength[]`):

    Column widths. An argument can be:

    - `int` or `double` - `System.Windows.Controls.ColumnDefinition.Width`. Value 0 means auto-size. Negative value is star-width, ie fraction of total width of star-sized columns. Examples: `50`, `-0.5`.
    - `System.Range` - `System.Windows.Controls.ColumnDefinition.MinWidth` and/or `System.Windows.Controls.ColumnDefinition.MaxWidth`. Sets width value = -1 (star-sized). Examples: `50..150`, `50..` or `..150`.
    - tuple `(double value, Range minMax)` - width and min/max widths. Example: `(-2, 50..)`.
    - `System.Windows.Controls.ColumnDefinition`.