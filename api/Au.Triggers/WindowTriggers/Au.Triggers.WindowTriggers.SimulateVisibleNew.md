# Method `Au.Triggers.WindowTriggers.SimulateVisibleNew`

Simulates event "visible new window" as if the specified window is that window. Similar to `Au.Triggers.WindowTriggers.SimulateActiveNew`.

```
public void SimulateVisibleNew(wnd w)
```

##### Parameters

- *w*  (`Au.wnd`)

##### Exceptions

- `InvalidOperationException`:
    Called before or after `Au.Triggers.ActionTriggers.Run`.

#### Remarks

Cannot be called before or after `Au.Triggers.ActionTriggers.Run`.