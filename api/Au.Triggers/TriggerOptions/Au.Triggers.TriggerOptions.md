# Class `Au.Triggers.TriggerOptions`

Allows to set some options for multiple triggers and their actions.

```
public class TriggerOptions
```

##### Remarks

You set options through a thread-static property `Au.Triggers.ActionTriggers.Options`. Changed options are applied to all triggers/actions added afterwards in this thread.

##### Examples

```
Triggers.Options.ThreadNew();
Triggers.Options.BeforeAction = o => { opt.key.KeySpeed = 10; };
Triggers.Hotkey["Ctrl+K"] = o => print.it(opt.key.KeySpeed); //10
Triggers.Hotkey["Ctrl+Shift+K"] = o => print.it(opt.key.KeySpeed); //10
Triggers.Options.BeforeAction = o => { opt.key.KeySpeed = 20; };
Triggers.Hotkey["Ctrl+L"] = o => print.it(opt.key.KeySpeed); //20
Triggers.Hotkey["Ctrl+Shift+L"] = o => print.it(opt.key.KeySpeed); //20
```

##### Inheritance

`object` → `TriggerOptions`

### Properties

`AfterAction`, `BeforeAction`, `EnabledAlways`

### Methods

`Reset`, `Thread`, `ThreadNew`, `ThreadOfTriggers`, `ThreadPool`, `ThreadThis`