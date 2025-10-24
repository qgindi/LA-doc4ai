# Class `Au.wndChildFinder`

Finds window controls (child windows). Contains name and other parameters of controls to find.

```
public class wndChildFinder
```

##### Remarks

Can be used instead of `Au.wnd.Child` or `Au.wnd.ChildAll`. Also can be used to find window that contains certain control, like in examples.

##### Examples

Find window that contains certain control, and get the control too.

```
var cf = new wndChildFinder("Password*", "Static");
wnd w = wnd.find(cn: "#32770", also: t => t.HasChild(cf));
print.it(w);
print.it(cf.Result);
```

The same with parameter *contains*.

```
var cf = new wndChildFinder("Password*", "Static");
wnd w = wnd.find(cn: "#32770", contains: cf);
print.it(w);
print.it(cf.Result);
```

##### Inheritance

`object` → `wndChildFinder`

### Constructors

`wndChildFinder(string, string, WCFlags, int?, Func<wnd, bool>, int)`

### Properties

`Result`

### Methods

`Exists`, `Exists`, `Find`, `Find`, `FindAll`, `FindAllInList`, `FindInList`, `IsMatch`, `ToString`