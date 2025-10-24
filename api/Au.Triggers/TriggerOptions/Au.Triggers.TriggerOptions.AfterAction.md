# Property `Au.Triggers.TriggerOptions.AfterAction`

A function to run after the trigger action. For example, it can log exceptions.

```
public Action<TOBAArgs> AfterAction { set; }
```

##### Property Value

`Action<Au.Triggers.TOBAArgs>`

#### Examples

```
Triggers.Options.AfterAction = o => { if(o.Exception!=null) print.it(o.Exception.Message); else print.it("completed successfully"); };
```