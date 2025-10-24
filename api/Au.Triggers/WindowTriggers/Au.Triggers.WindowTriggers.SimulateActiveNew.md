# Method `Au.Triggers.WindowTriggers.SimulateActiveNew`

Simulates event "activated new window" as if the specified window is that window.

```
public void SimulateActiveNew(wnd w)
```

##### Parameters

- *w*  (`Au.wnd`)

##### Exceptions

- `InvalidOperationException`:
    Called before or after `Au.Triggers.ActionTriggers.Run`.

#### Remarks

This function usually is used to run `ActiveNew` triggers for a window created before calling `Au.Triggers.ActionTriggers.Run`. Here "run triggers" means "compare window properties etc with those specified in triggers and run actions of triggers that match". Normally such triggers don't run because the window is considered old. This function runs triggers as it was a new window. Triggers like `ActiveNew` and `ActiveOnce` will run once, as usually. This function must be called while the main triggers thread is in `Au.Triggers.ActionTriggers.Run`, for example from another trigger action. It is asynchronous (does not wait). If called from a trigger action (hotkey etc), make sure the window trigger action runs in another thread or can be queued. Else both actions cannot run simultaneously. See example.

#### Examples

Note: the `Triggers` in examples is a field or property of type `Au.Triggers.ActionTriggers`.

```
Triggers.Options.ThreadNew(true);
Triggers.Window[TWEvent.ActiveNew, "* Notepad"] = o => o.Window.Resize(500, 200);
Triggers.Hotkey["Ctrl+T"] = o => Triggers.Window.SimulateActiveNew(wnd.active);
```