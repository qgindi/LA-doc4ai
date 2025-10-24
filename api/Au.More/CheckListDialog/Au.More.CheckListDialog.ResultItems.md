# Property `Au.More.CheckListDialog.ResultItems`

Gets strings of checked items. This property is set by `Au.More.CheckListDialog.ShowDialog`.

```
public string[] ResultItems { get; }
```

##### Property Value

`string[]`

#### Examples

```
List<string> a = ["one", "two"];
var d = new CheckListDialog("Info.");
d.Add(a);
if (!d.ShowDialog() || !d.ResultItems.Any()) return;
a = d.ResultItems.ToList();
```