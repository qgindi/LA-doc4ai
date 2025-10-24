# Enum `Au.Triggers.TWEvent`

Events for window triggers.

```
public enum TWEvent
```

##### Remarks

Cloaked windows are considered invisible. See `Au.wnd.IsCloaked`.

The "active" events don't occur if/while the activated window is invisible. To catch invisible windows too, use a `Au.More.WinEventHook` instead of a trigger. See example.

##### Examples

How to use a hook instaed of a window trigger. This code can be in the same file as your window triggers.

```
new WinEventHook(EEvent.SYSTEM_FOREGROUND, 0, k => {
	print.it(k.w);
	if (k.w.IsMatch("* Name", "classname")) { print.it("fast code can be here", k.w); };
	//if (k.w.IsMatch("* Name", "classname")) run.thread(() => { print.it("slower code can be here", k.w); });
	//if (k.w.IsMatch("* Name", "classname")) script.run("large code.cs", k.w.Handle.ToS());
});
```

### Fields

| Name | Description |
| --- | --- |
| Active | When the specified window becomes active (each time). |
| ActiveNew | When the specified window is created and then becomes active. The same as `Au.Triggers.TWEvent.ActiveOnce`, but windows created before calling `Au.Triggers.ActionTriggers.Run` are ignored. |
| ActiveOnce | When the specified window becomes active the first time in the trigger's life. |
| Visible | When the specified window becomes visible (each time). |
| VisibleNew | When the specified window is created and then becomes visible. The same as `Au.Triggers.TWEvent.VisibleOnce`, but windows created before calling `Au.Triggers.ActionTriggers.Run` are ignored. |
| VisibleOnce | When the specified window becomes visible the first time in the trigger's life. |