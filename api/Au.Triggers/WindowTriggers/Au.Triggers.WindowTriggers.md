# Class `Au.Triggers.WindowTriggers`

Window triggers.

```
public class WindowTriggers : IEnumerable<WindowTrigger>
```

##### Examples

Note: the `Triggers` in examples is a field or property like `readonly ActionTriggers Triggers = new();`.

```
var wt = Triggers.Window; //wt is a WindowTriggers instance
wt[TWEvent.ActiveNew, "Window name"] = o => print.it(o.Window);
wt[TWEvent.Visible, "Window2 name"] = o => print.it(o.Window);
Triggers.Run();
```

More examples: `Au.Triggers.ActionTriggers`.

##### Inheritance

`object` → `WindowTriggers`

### Properties

`this[TWEvent, wndFinder, TWFlags, TWLater, string, int]`, `this[TWEvent, string, string, WOwner, Func<wnd, bool>, WContains, TWFlags, TWLater, string, int]`, `Last`

### Methods

`GetEnumerator`, `LogEvents`, `SimulateActiveNew`, `SimulateVisibleNew`