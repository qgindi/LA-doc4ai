# Property `Au.Triggers.TriggerOptions.AfterAction`

A function to run after the trigger action.
For example, it can log exceptions.

```csharp
public Action<TOBAArgs> AfterAction { set; }
```

##### Property Value

`Action<Au.Triggers.TOBAArgs>`

#### Examples

```csharp
Triggers.Options.AfterAction = o => { if(o.Exception!=null) print.it(o.Exception.Message); else print.it("completed successfully"); };
```