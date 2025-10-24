# Class `Au.wndFinder`

Finds top-level windows (`Au.wnd`). Contains name and other parameters of windows to find.

```
public class wndFinder
```

##### Remarks

Can be used instead of `Au.wnd.find` or `Au.wnd.findAll`. These codes are equivalent:

```
wnd w = wnd.find(a, b, c, d, e); if(!w.Is0) print.it(w);
```

```
var p = new wndFinder(a, b, c, d, e); if(p.Exists()) print.it(p.Result);
```

Also can find in a list of windows.

##### Inheritance

`object` → `wndFinder`

### Constructors

`wndFinder(string, string, WOwner, WFlags, Func<wnd, bool>, WContains)`

### Properties

`Props`, `Result`

### Methods

`Exists`, `Exists`, `Find`, `Find`, `FindAll`, `FindAllInList`, `FindInList`, `IsMatch`, `ToString`, `Wait`