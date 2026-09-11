# Property `Au.More.CheckListDialog.ResultItems`

Gets strings of checked items.
This property is set by`Au.More.CheckListDialog.ShowDialog`.

```csharp
public string[] ResultItems { get; }
```

##### Property Value

`string[]`

#### Examples

```csharp
List<string> a = ["one", "two"];
var d = new CheckListDialog("Info.");
d.Add(a);
if (!d.ShowDialog() || !d.ResultItems.Any()) return;
a = d.ResultItems.ToList();
```