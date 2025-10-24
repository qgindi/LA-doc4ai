# Class `Au.More.WinEventHook`

Helps with UI element event hooks. See API `SetWinEventHook`.

```
public sealed class WinEventHook : IDisposable
```

##### Remarks

The thread that uses hooks must process Windows messages. For example have a window/dialog/messagebox, or use a "wait-for" function that dispatches messages or has such option (see `Au.Types.Seconds.DoEvents`).

> **Important:**
> The variable should be disposed when don't need, or at least unhooked, either explicitly (call `Au.More.WinEventHook.Dispose` or `Au.More.WinEventHook.Unhook` in same thread) or with `using`. Can do it in hook procedure.

##### Examples

```
bool stop = false;
using var hook = new WinEventHook(EEvent.SYSTEM_FOREGROUND, 0, x => {
	print.it(x.event_, x.w);
	var e = x.GetElm();
	print.it(e);
	if(x.w.ClassNameIs("Shell_TrayWnd")) stop = true;
});
dialog.show("hook");
//or
//wait.doEventsUntil(-10, () => stop); //wait max 10 s for activated taskbar
//print.it("the end");
```

##### Inheritance

`object` → `WinEventHook`

### Constructors

`WinEventHook(EEvent, EEvent, Action<WinEvent>, int, int, EHookFlags)`, `WinEventHook(EEvent[], Action<WinEvent>, int, int, EHookFlags)`

### Methods

`Add`, `Dispose`, `Hook`, `Hook`, `Remove`, `Unhook`