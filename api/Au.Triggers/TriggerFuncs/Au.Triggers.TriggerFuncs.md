# Class `Au.Triggers.TriggerFuncs`

Allows to define custom scopes/contexts/conditions for triggers.

```
public class TriggerFuncs
```

##### Remarks

Similar to `Au.Triggers.TriggerScopes` (code like `Triggers.Of.Window(...);`), but allows to define any scope/condition/etc, not just the active window.

To define a scope, you create a callback function (CF) that checks some conditions and returns `true` to allow the trigger action to run or `false` to not allow. Assign the CF to some property of this class and then add the trigger, like in the examples below. The CF will be assigned to the trigger and called when need.

You may ask: why to use CF when the trigger action (TA) can do the same?

1. CF runs synchronously; if it returns `false`, the trigger key or mouse button message is passed to other triggers, hooks and apps. TA cannot do it reliably; it runs asynchronously, and the message is already stealed from other apps/triggers/hooks.
2. CF is faster to call. It is simply called in the same thread that processes trigger messages. TA usually runs in another thread.
3. A CF can be assigned to multiple triggers with a single line of code. Don't need to add the same code in all trigger actions.

A trigger can have up to 4 CF delegates and a window scope (`Triggers.Of...`). They are called in this order: CF assigned through `Au.Triggers.TriggerFuncs.FollowingTriggersBeforeWindow`, `Au.Triggers.TriggerFuncs.NextTriggerBeforeWindow`, window scope, `Au.Triggers.TriggerFuncs.NextTrigger`, `Au.Triggers.TriggerFuncs.FollowingTriggers`. The `NextX` properties assign the CF to the next single trigger. The `FollowingX` properties assign the CF to all following triggers until you assign another CF or `null`. If several are assigned, the trigger action runs only if all CF return `true` and the window scope matches. The `XBeforeWindow` properties are used only with hotkey, autotext and mouse triggers.

All CF must be as fast as possible. Slow CF can make triggers slower (or even all keyboard/mouse input); also may cause warnings and trigger failures. A big problem is the low-level hooks timeout that Windows applies to trigger hooks; see `Au.More.WindowsHook.LowLevelHooksTimeout`. A related problem - slow JIT and loading of assemblies, which can make the CF too slow the first time; in some rare cases may even need to preload assemblies or pre-JIT functions to avoid the timeout warning.

In CF never use functions that generate keyboard or mouse events or activate windows.

##### Examples

Note: the `Triggers` in examples is a field or property like `readonly ActionTriggers Triggers = new();`.

```
//examples of assigning a callback function (CF) to a single trigger
Triggers.FuncOf.NextTrigger = o => keys.isCapsLock; //o => keys.isCapsLock is the callback function (lambda)
Triggers.Hotkey["Ctrl+K"] = o => print.it("action: Ctrl+K while CapsLock is on");
Triggers.FuncOf.NextTrigger = o => { var v = o as HotkeyTriggerArgs; print.it($"func: mod={v.Mod}"); return mouse.isPressed(MButtons.Left); };
Triggers.Hotkey["Ctrl+Shift?+B"] = o => print.it("action: mouse left button + Ctrl+B or Ctrl+Shift+B");

//examples of assigning a CF to multiple triggers
Triggers.FuncOf.FollowingTriggers = o => { var v = o as HotkeyTriggerArgs; print.it("func", v); return true; };
Triggers.Hotkey["Ctrl+F8"] = o => print.it("action: " + o);
Triggers.Hotkey["Ctrl+F9"] = o => print.it("action: " + o);
Triggers.FuncOf.FollowingTriggers = null; //stop assigning the CF to triggers added afterwards

//sometimes all work can be done in CF and you don't need the trigger action
Triggers.FuncOf.NextTrigger = o => { var v = o as HotkeyTriggerArgs; print.it("func: " + v); return true; };
Triggers.Hotkey["Ctrl+F12"] = null;

Triggers.Run();
```

##### Inheritance

`object` → `TriggerFuncs`

### Properties

`FollowingTriggers`, `FollowingTriggersBeforeWindow`, `NextTrigger`, `NextTriggerBeforeWindow`

### Methods

`Reset`