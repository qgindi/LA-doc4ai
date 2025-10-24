# Method `Au.Triggers.ActionTriggers.ShowTriggersListWindow`

Shows a temporary window with a list of currently active triggers for the active window (hotkey, autotext and mouse edge/move triggers) or the mouse window (mouse click/wheel triggers).

```
public void ShowTriggersListWindow(int triggerType = -1)
```

##### Parameters

- *triggerType*  (`int`):
    Which trigger type to select initially: 0 hotkey, 1 autotext, 2 mouse, 3 window, -1 previous.

#### Remarks

To determine which triggers are active in the target window, the function uses window scopes specified in code (like `Triggers.Of.Window("Window name")`). However it ignores code like `Triggers.FuncOf...`, therefore the list includes triggers deactivated by your `FuncOf` functions.

#### Examples

Code in file `Hotkey triggers.cs`. Calls this function when pressed hotkey `Alt+?`.

```
hk["Alt+?"] = o => Triggers.ShowTriggersListWindow();
```