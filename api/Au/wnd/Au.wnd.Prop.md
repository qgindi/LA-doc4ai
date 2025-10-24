# Property `Au.wnd.Prop`

Returns an object that manages window properties using API `SetProp` and co.

```
public WProp Prop { get; }
```

##### Property Value

`Au.Types.WProp`

#### Examples

```
var w = wnd.find("* Explorer");
w.Prop.Set("example", 5);
print.it(w.Prop["example"]);
print.it(w.Prop); //all w properties
w.Prop.Remove("example"); //you should always remove window properties if don't want to see unrelated applications crashing after some time. And don't use many unique property names.
```