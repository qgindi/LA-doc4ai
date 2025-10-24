# Method `Au.More.WindowsHook.ThreadCbt`

Sets a `WH_CBT` hook for a thread of this process. See API `SetWindowsHookEx`.

```
public static WindowsHook ThreadCbt(Func<HookData.ThreadCbt, bool> hookProc, int threadId = 0, bool setNow = true)
```

##### Parameters

- *hookProc*  (`Func<Au.Types.HookData.Au.Types.HookData.ThreadCbt, bool>`):

    Hook procedure (function that handles hook events). Must return as soon as possible. If returns `true`, the event is canceled. For some events you can modify some fields of event data.

    > **Note:**
    >     When the hook procedure returns, the parameter variable becomes invalid and unsafe to use. If you need the data for later use, copy its properties and not the variable.
- *threadId*  (`int`):
    Native thread id, or 0 for this thread. The thread must belong to this process.
- *setNow*  (`bool`):
    Set hook now. Default `true`.

##### Returns

`Au.More.WindowsHook`

New `Au.More.WindowsHook` object that manages the hook.

##### Exceptions

- `Au.Types.AuException`:
    Failed.

#### Examples

```
using var hook = WindowsHook.ThreadCbt(x => {
	print.it(x.code);
	switch(x.code) {
	case HookData.CbtEvent.ACTIVATE:
		print.it(x.Hwnd);
		break;
	case HookData.CbtEvent.CREATEWND:
		var c=x.CreationInfo->lpcs;
		print.it(x.Hwnd, c->x, c->lpszName);
		c->x=500;
		break;
	}
	return false;
});
dialog.showOkCancel("hook");
//new Form().ShowDialog(); //to test MINMAX
```