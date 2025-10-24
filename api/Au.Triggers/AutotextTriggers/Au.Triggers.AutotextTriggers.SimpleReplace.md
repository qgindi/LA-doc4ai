# Property `Au.Triggers.AutotextTriggers.SimpleReplace`

Allows to add triggers in a more concise way - assign a string, not a function. The string will replace the user-typed text.

```
public TASimpleReplace SimpleReplace { get; }
```

##### Property Value

`Au.Triggers.TASimpleReplace`

#### Examples

```
var ts = Triggers.Autotext.SimpleReplace;
ts["#su"] = "Sunday"; //the same as Triggers.Autotext["#su"] = o => o.Replace("Sunday");
ts["#mo"] = "Monday";
```