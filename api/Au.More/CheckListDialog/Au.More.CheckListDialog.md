# Class `Au.More.CheckListDialog`

Dialog with list of check boxes.

```
public class CheckListDialog
```

##### Examples

```
string[] a = ["one", "two"];
var d = new CheckListDialog("Info.");
d.Add(a);
d.Add("three", true);
d.Add("four");
if (!d.ShowDialog()) return;
print.it(d.ResultBits, d.ResultIndices, d.ResultItems);
```

##### Inheritance

`object` → `CheckListDialog`

### Constructors

`CheckListDialog(string, string)`

### Properties

`Builder`, `ResultBits`, `ResultIndices`, `ResultItems`

### Methods

`Add`, `Add`, `FormatText`, `SetButtons`, `ShowDialog`

### See Also

`Au.More.EnumUI<TEnum>`