# Method `Au.Triggers.TriggerOptions.ThreadThis`

Run trigger actions in this thread (which called this function).

```
public void ThreadThis()
```

#### Remarks

This function can be used only if `Au.Triggers.ActionTriggers.Run` runs in another thread. This thread must have a message loop (wait and dispatch messages). For it can be used `Au.Triggers.ActionTriggers.RunThread`.

Trigger actions should be fast, else other trigger actions may be delayed. If a trigger action dispatches messages, other trigger actions can run in the meantime.

Can be used to create and show toolbars (`Au.toolbar`). Used in the default `"Triggers and toolbars"` script since v0.16.

#### Examples

```
print.it(Environment.CurrentManagedThreadId);
ActionTriggers Triggers = new();
Triggers.Options.ThreadThis();
Triggers.Hotkey["F11"] = o => { print.it(Environment.CurrentManagedThreadId); };
Triggers.RunThread();
```