# Property `Au.Triggers.ActionTriggers.Disabled`

Gets or sets whether triggers of this `Au.Triggers.ActionTriggers` instance are disabled.

```
public bool Disabled { get; set; }
```

##### Property Value

`bool`

#### Remarks

Does not depend on `Au.Triggers.ActionTriggers.DisabledEverywhere`. Does not end/pause threads of trigger actions.

#### Examples

Note: the `Triggers` in examples is a field or property like `readonly ActionTriggers Triggers = new();`.

```
Triggers.Hotkey["Ctrl+T"] = o => print.it("Ctrl+T");
Triggers.Hotkey["Ctrl+D"] = o => { print.it("Ctrl+D (disable/enable)"); Triggers.Disabled ^= true; }; //toggle
Triggers.Hotkey.Last.EnabledAlways = true;
Triggers.Run();
```

### See Also

`Au.Triggers.ActionTrigger.EnabledAlways`

`Au.Triggers.TriggerOptions.EnabledAlways`