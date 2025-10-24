# Property `Au.More.CheckListDialog.Builder`

Gets the `Au.wpfBuilder` that builds the dialog. You can use it to add more controls, change window properties, etc; see example.

```
public wpfBuilder Builder { get; }
```

##### Property Value

`Au.wpfBuilder`

#### Examples

```
using System.Windows.Controls;
string[] a = ["one", "two"];
var d = new CheckListDialog("Info.");
d.Add(a);
d.Builder.R.Add("Input", out TextBox tInput);
if (!d.ShowDialog()) return;
print.it(d.ResultBits, d.ResultIndices, d.ResultItems, tInput.Text);
```