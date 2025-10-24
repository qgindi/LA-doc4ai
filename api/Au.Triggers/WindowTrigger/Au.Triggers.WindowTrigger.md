# Class `Au.Triggers.WindowTrigger`

Represents a window trigger.

```
public class WindowTrigger : ActionTrigger
```

##### Examples

```
Triggers.Window[TWEvent.ActiveNew, "Window name"] = o => print.it(o.Window);
var v = Triggers.Window.Last; //v is the new WindowTrigger. Rarely used.
```

##### Inheritance

`object` → `Au.Triggers.ActionTrigger` → `WindowTrigger`

### Properties

`Event`, `Finder`, `Flags`, `Later`, `ParamsString`, `TypeString`

### Members inherited from other types of this library
`ActionTrigger.Scope`, `ActionTrigger.SourceFile`, `ActionTrigger.SourceLine`, `ActionTrigger.ToString()`, `ActionTrigger.Disabled`, `ActionTrigger.DisabledThisOrAll`, `ActionTrigger.EnabledAlways`, `ActionTrigger.RunAction()`