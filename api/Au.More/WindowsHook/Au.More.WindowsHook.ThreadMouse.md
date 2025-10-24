# Method `Au.More.WindowsHook.ThreadMouse`

Sets a `WH_MOUSE` hook for a thread of this process. See API `SetWindowsHookEx`.

```
public static WindowsHook ThreadMouse(Func<HookData.ThreadMouse, bool> hookProc, int threadId = 0, bool setNow = true)
```

##### Parameters

- *hookProc*  (`Func<Au.Types.HookData.Au.Types.HookData.ThreadMouse, bool>`):

    The hook procedure (function that handles hook events). Must return as soon as possible. If returns `true`, the event is canceled.

    > **Note:**
    >     When the hook procedure returns, the pointer field of the parameter variable becomes invalid and unsafe to use.
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
using var hook = WindowsHook.ThreadMouse(x => {
	print.it(x.message, x.m->pt, x.m->hwnd, x.PM_NOREMOVE);
	return false;
});
dialog.show("hook");
```