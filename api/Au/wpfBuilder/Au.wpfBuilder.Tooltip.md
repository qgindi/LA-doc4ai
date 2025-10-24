# Method `Au.wpfBuilder.Tooltip`

Sets tooltip text/content/object of the last added element. See `System.Windows.FrameworkElement.ToolTip`.

```
public wpfBuilder Tooltip(object tooltip)
```

##### Parameters

- *tooltip*  (`object`):
    Tooltip text (string), or tooltip content element, or `System.Windows.Controls.ToolTip` object.

##### Returns

`Au.wpfBuilder`

#### Examples

Text box with simple tooltip.

```
b.R.Add("Example", out TextBox _).Tooltip("Tooltip text");
```

Tooltip with content created by another `Au.wpfBuilder`.

```
//tooltip content
var btt = new wpfBuilder()
	.R.Add<Image>().Image(icon.stock(StockIcon.INFO).ToWpfImage())
	.R.Add<TextBlock>().Text("Some ", "<b>text", ".")
	.End();
//dialog
var b = new wpfBuilder("Window").WinSize(300);
b.R.AddButton("Example", null).Tooltip(btt.Panel);
b.R.AddOkCancel();
b.End();
if (!b.ShowDialog()) return;
```