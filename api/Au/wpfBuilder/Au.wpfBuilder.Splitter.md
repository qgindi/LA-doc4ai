# Method `Au.wpfBuilder.Splitter`

Sets vertical or horizontal splitter properties of the last added `System.Windows.Controls.GridSplitter`.

```
public wpfBuilder Splitter(bool vertical, int span = 1, double thickness = 4)
```

##### Parameters

- *vertical*  (`bool`):
    If `true`, resizes columns, else rows.
- *span*  (`int`):
    How many rows spans vertical splitter, or how many columns spans horizontal splitter. Can be more than row/column count.
- *thickness*  (`double`):
    Width of vertical splitter or height of horizontal. If `double.NaN`, sets alignment "stretch", else "center".

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    The last added element is not `System.Windows.Controls.GridSplitter`.

#### Examples

Vertical splitter.

```
var b = new wpfBuilder("Window").WinSize(400)
	.Columns(30.., 0, -1) //the middle column is for splitter; the 30 is minimal width
	.R.Add(out TextBox _)
	.Add<GridSplitter>().Splitter(true, 2).Brush(Brushes.Orange) //add splitter in the middle column
	.Add(out TextBox _)
	.R.Add(out TextBox _).Skip().Add(out TextBox _) //skip the splitter's column
	.R.AddOkCancel()
	.End();
if (!b.ShowDialog()) return;
```

Horizontal splitter.

```
var b = new wpfBuilder("Window").WinSize(300, 300)
	.Row(27..).Add("Row", out TextBox _)
	.Add<GridSplitter>().Splitter(false, 2).Brush(Brushes.Orange)
	.Row(-1).Add("Row", out TextBox _)
	.R.AddOkCancel()
	.End();
if (!b.ShowDialog()) return;
```