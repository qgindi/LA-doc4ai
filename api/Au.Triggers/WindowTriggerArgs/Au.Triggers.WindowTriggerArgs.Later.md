# Property `Au.Triggers.WindowTriggerArgs.Later`

The "later" event, or 0 if it is the primary trigger (`ActiveNew` etc). See example.

```csharp
public TWLater Later { get; }
```

##### Property Value

`Au.Triggers.TWLater`

#### Examples

Note: the `Triggers` in examples is a field or property like `readonly ActionTriggers Triggers = new();`.

```csharp
Triggers.Window[TWEvent.ActiveOnce, "*- Paint", later: TWLater.Active | TWLater.Inactive] = o => { print.it(o.Later, o.Window); };
Triggers.Run();
```