# Class `Au.elmFinder`

Finds UI elements (`Au.elm`). Contains name and other parameters of elements to find.

```
public class elmFinder
```

##### Examples

Find link `"Example"` in web page, and click. Wait max 5 s. Exception if not found.

```
var w = wnd.find(0, "* Chrome");
w.Elm["web:LINK", "Example"].Find(5).Invoke();
```

Find window that contains certain UI element, and get the UI element too.

```
var f = new elmFinder("BUTTON", "Apply"); //or var f = elm.path["BUTTON", "Apply"];
wnd w = wnd.find(cn: "#32770", also: t => f.In(t).Exists()); //or t => t.HasElm(f)
print.it(w);
print.it(f.Result);
```

##### Inheritance

`object` → `elmFinder`

### Constructors

`elmFinder(string, string, Strings, EFFlags, Func<elm, bool>, int, string)`

### Properties

`this[string, string, Strings, EFFlags, Func<elm, bool>, int, string]`, `Next`, `Result`, `ResultGetProperty`, `ResultProperty`

### Methods

`Exists`, `Exists`, `Find`, `Find`, `FindAll`, `In`, `In`, `ToString`, `Wait`