# Property `Au.Triggers.TriggerOptions.BeforeAction`

A function to run before the trigger action. For example, it can set `Au.opt` options.

```
public Action<TOBAArgs> BeforeAction { set; }
```

##### Property Value

`Action<Au.Triggers.TOBAArgs>`

#### Examples

```
Triggers.Options.BeforeAction = o => { opt.key.KeySpeed = 20; opt.key.TextSpeed = 5; };
```