# Class `Au.Triggers.ActionTriggers`

The main class of action triggers.

```
public class ActionTriggers
```

##### Remarks

This class manages action triggers. Action triggers are used to call functions (aka *trigger actions*) in a running script in response to events such as hotkey, typed text, mouse action, activated window. To launch scripts are used other ways: manually, at startup, command line, `Au.script.run`, output link.

If your script has a variable, field or property like `ActionTriggers Triggers = new();`, through it you can access all trigger types (hotkey, window, etc) and add triggers to them.

Code syntax to add an action trigger:

```
Triggers.TriggerType[parameters] = action;
```

Examples:

```
Triggers.Hotkey["Ctrl+K"] = o => print.it(o);
Triggers.Hotkey["Ctrl+Shift+K"] = o => {
	print.it("This is a trigger action (lambda function).");
	print.it($"It runs when you press {o}.");
};
Triggers.Run();
```

Also you can set options (`Au.Triggers.TriggerOptions`), window scopes (`Au.Triggers.TriggerScopes`) and custom scopes (`Au.Triggers.TriggerFuncs`) for triggers added afterwards.

Finally call `Au.Triggers.ActionTriggers.Run` or `Au.Triggers.ActionTriggers.RunThread`. It runs all the time and launches trigger actions (functions) when need. Actions run in other thread(s) by default.

To quickly restart the script when editing, click the **Run** button.

Avoid multiple scripts with triggers. Each running instance uses some CPU. All triggers should be in single script, if possible. It's OK to run additional scripts temporarily, for example to test new triggers without restarting the main script. From trigger actions you can call `Au.script.run` to run other scripts in new process; see example.

Trigger actions may not inherit `Au.opt` options that are set before adding triggers. The example shows how to correctly set `Au.opt` options for multiple actions. Also you can set them in action code. Next action running in the same thread will not inherit `Au.opt` options set by previous action.

##### Examples

This is a single script with many action triggers.

```
using Au.Triggers;

ActionTriggers Triggers = new();
//readonly ActionTriggers Triggers = new(); //or add this field if you'll use triggers in a class

//you can set options for triggers added afterwards
Triggers.Options.Thread(0, 500);

//you can use variables if don't want to type "Triggers.Hotkey" etc for each trigger
var hk = Triggers.Hotkey;
var mouse = Triggers.Mouse;
var win = Triggers.Window;
var tt = Triggers.Autotext;

//hotkey triggers

hk["Ctrl+K"] = o => print.it(o); //it means: execute code "o => print.it(o)" when I press Ctrl+K
hk["Ctrl+Shift+F11"] = o => {
	print.it(o);
	var w1 = wnd.findOrRun("* Notepad", run: () => run.it(folders.System + "notepad.exe"));
	keys.sendt("text");
	w1.Close();
};
hk["Win+Alt+K"] = o => script.run("Example.cs"); //run another script in new process

//triggers that work only with some windows

Triggers.Of.Window("* Chrome", "Chrome_WidgetWin_1"); //let the following triggers work only when a Chrome window is active
hk["Ctrl+F5"] = o => print.it(o, o.Window);
hk["Ctrl+F6"] = o => print.it(o, o.Window);

var notepad = Triggers.Of.Window("* Notepad"); //let the following triggers work only when a Notepad window is active
hk["Ctrl+F5"] = o => print.it(o, o.Window);
hk["Ctrl+F6"] = o => print.it(o, o.Window);

Triggers.Of.AllWindows(); //let the following triggers work with all windows

//mouse triggers

mouse[TMClick.Right, "Ctrl+Shift", TMFlags.ButtonModUp] = o => print.it(o);
mouse[TMEdge.RightInCenter50] = o => { print.it(o); dialog.show("Bang!", x: Coord.Max); };
mouse[TMMove.LeftRightInCenter50] = o => wnd.switchActiveWindow();

Triggers.FuncOf.NextTrigger = o => keys.isScrollLock; //example of a custom scope (aka context, condition)
mouse[TMWheel.Forward] = o => print.it($"{o} while ScrollLock is on");

Triggers.Of.Again(notepad); //let the following triggers work only when a Notepad window is active
mouse[TMMove.LeftRightInBottom25] = o => { print.it(o); o.Window.Close(); };
Triggers.Of.AllWindows();

//window triggers. Note: window triggers don't depend on Triggers.Of.

win[TWEvent.ActiveNew, "* Notepad", "Notepad"] = o => print.it("opened Notepad window");
win[TWEvent.ActiveNew, "Notepad", "#32770", contains: "Do you want to save *"] = o => {
	print.it("opened Notepad's 'Do you want to save' dialog");
	//keys.send("Alt+S"); //click the Save button
};

//autotext triggers

tt["los"] = o => o.Replace("Los Angeles");
tt["WIndows", TAFlags.MatchCase] = o => o.Replace("Windows");
tt.DefaultPostfixType = TAPostfix.None;
tt["<b>"] = o => o.Replace("<b>[[|]]</b>");
tt["#file"] = o => {
	o.Replace("");
	var fd = new FileOpenSaveDialog();
	if(fd.ShowOpen(out string file)) keys.sendt(file);
};
tt.DefaultPostfixType = default;

//shorter auto-replace code

var ts = Triggers.Autotext.SimpleReplace;
ts["#so"] = "Some text"; //the same as tt["#so"] = o => o.Replace("Some text");
ts["#mo"] = "More text";

//how to set opt options for trigger actions

Triggers.Options.BeforeAction = o => { opt.key.TextHow = OKeyText.Paste; }; //sets opt before executing an action
ts["#p1"] = "text 1";
ts["#p2"] = "text 2";
Triggers.Options.BeforeAction = null;

//initial opt for ALL trigger actions also can be set ONCE when adding triggers. Use Triggers.Options.BeforeAction if want to override some options for some trigger actions.

opt.key.TextHow = OKeyText.Paste;
//then add all triggers

//how to stop and disable/enable triggers

hk["Ctrl+Alt+Q"] = o => Triggers.Stop(); //let Triggers.Run() end its work and return
hk.Last.EnabledAlways = true;

hk["Ctrl+Alt+D"] = o => Triggers.Disabled ^= true; //disable/enable triggers here
hk.Last.EnabledAlways = true;

hk["Ctrl+Alt+Win+D"] = o => ActionTriggers.DisabledEverywhere ^= true; //disable/enable triggers in all processes
hk.Last.EnabledAlways = true;

hk["Ctrl+F7"] = o => print.it("This trigger can be disabled/enabled with Ctrl+F8.");
var t1 = hk.Last;
hk["Ctrl+F8"] = o => t1.Disabled ^= true; //disable/enable a trigger

//finally call Triggers.Run(). Without it the triggers won't work.
Triggers.Run();
//Triggers.Run returns when is called Triggers.Stop (see the "Ctrl+Alt+Q" trigger above).
print.it("called Triggers.Stop");
```

##### Inheritance

`object` → `ActionTriggers`

### Constructors

`ActionTriggers()`

### Properties

`Autotext`, `Disabled`, `DisabledEverywhere`, `FuncOf`, `Hotkey`, `Mouse`, `Of`, `Options`, `Window`

### Methods

`ResetOptions`, `Run`, `RunThread`, `ShowTriggersListWindow`, `Stop`

### Events

`Stopping`