# Method `Au.Types.ExtWpf.AddRows`

Adds one or more rows. Like `Au.wpfBuilder.Row`.

```
public static void AddRows(this Grid g, params WBGridLength[] heights)
```

##### Parameters

- *g*  (`Grid`)
- *heights*  (`Au.Types.WBGridLength[]`):

    Row height. Can be:

    - `int` or `double` - `System.Windows.Controls.RowDefinition.Height`. Value 0 means auto-size. Negative value is star-width, ie fraction of total height of star-sized rows. Examples: `50`, `-0.5`.
    - `System.Range` - `System.Windows.Controls.RowDefinition.MinHeight` and/or `System.Windows.Controls.RowDefinition.MaxHeight`. Sets height value = -1 (star-sized). Examples: `50..150`, `50..` or `..150`.
    - tuple `(double value, Range minMax)` - height and min/max heights. Example: `(-2, 50..200)`.
    - `System.Windows.Controls.RowDefinition`.