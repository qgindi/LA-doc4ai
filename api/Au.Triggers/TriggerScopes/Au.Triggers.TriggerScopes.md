# Class `Au.Triggers.TriggerScopes`

Allows to specify working windows for multiple triggers of these types: hotkey, autotext, mouse.

```
public class TriggerScopes
```

##### Examples

Note: the `Triggers` in examples is a field or property like `readonly ActionTriggers Triggers = new();`.

```
Triggers.Hotkey["Ctrl+K"] = o => print.it("this trigger works with all windows");
Triggers.Of.Window("* Notepad"); //specifies a working window for triggers added afterwards
Triggers.Hotkey["Ctrl+F11"] = o => print.it("this trigger works only when a Notepad window is active");
Triggers.Hotkey["Ctrl+F12"] = o => print.it("this trigger works only when a Notepad window is active");
var chrome = Triggers.Of.Window("* Chrome"); //specifies another working window for triggers added afterwards
Triggers.Hotkey["Ctrl+F11"] = o => print.it("this trigger works only when a Chrome window is active");
Triggers.Hotkey["Ctrl+F12"] = o => print.it("this trigger works only when a Chrome window is active");
Triggers.Of.AllWindows(); //let triggers added afterwards work with all windows
Triggers.Mouse[TMEdge.RightInTop25] = o => print.it("this trigger works with all windows");
Triggers.Of.Again(chrome); //sets a previously specified working window for triggers added afterwards
Triggers.Mouse[TMEdge.RightInBottom25] = o => print.it("this trigger works only when a Chrome window is active");
Triggers.Mouse[TMMove.DownUp] = o => print.it("this trigger works only when a Chrome window is active");
Triggers.Mouse[TMClick.Middle] = o => print.it("this trigger works only when the mouse is in a Chrome window");
Triggers.Mouse[TMWheel.Forward] = o => print.it("this trigger works only when the mouse is in a Chrome window");
Triggers.Run();
```

##### Inheritance

`object` → `TriggerScopes`

### Methods

`Again`, `AllWindows`, `NotWindow`, `NotWindow`, `NotWindows`, `Window`, `Window`, `Windows`