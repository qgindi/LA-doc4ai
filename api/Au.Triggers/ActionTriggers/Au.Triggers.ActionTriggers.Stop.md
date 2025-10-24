# Method `Au.Triggers.ActionTriggers.Stop`

Stops trigger engines and causes `Au.Triggers.ActionTriggers.Run` to return.

```
public void Stop()
```

#### Remarks

Does not abort threads of trigger actions that are still running.

#### Examples

Note: the `Triggers` in examples is a field or property like `readonly ActionTriggers Triggers = new();`.

```
Triggers.Hotkey["Ctrl+T"] = o => print.it("Ctrl+T");
Triggers.Hotkey["Ctrl+Q"] = o => { print.it("Ctrl+Q (stop)"); Triggers.Stop(); };
Triggers.Hotkey.Last.EnabledAlways = true;
Triggers.Run();
print.it("stopped");
```