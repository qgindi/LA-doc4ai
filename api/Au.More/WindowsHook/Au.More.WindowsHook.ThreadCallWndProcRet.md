# Method `Au.More.WindowsHook.ThreadCallWndProcRet`

Sets a `WH_CALLWNDPROCRET` hook for a thread of this process. See API `SetWindowsHookEx`.

```
public static WindowsHook ThreadCallWndProcRet(Action<HookData.ThreadCallWndProcRet> hookProc, int threadId = 0, bool setNow = true)
```

##### Parameters

- *hookProc*  (`Action<Au.Types.HookData.Au.Types.HookData.ThreadCallWndProcRet>`):

    The hook procedure (function that handles hook events). Must return as soon as possible. The event cannot be canceled or modified.

    > **Note:**
    >     When the hook procedure returns, the pointer field of the parameter variable becomes invalid and unsafe to use.
- *threadId*  (`int`):
    Native thread id, or 0 for this thread. The thread must belong to this process.
- *setNow*  (`bool`):
    Set hook now. Default `true`.

##### Returns

`Au.More.WindowsHook`

A new `Au.More.WindowsHook` object that manages the hook.

##### Exceptions

- `Au.Types.AuException`:
    Failed.

#### Examples

```
using var hook = WindowsHook.ThreadCallWndProc(x => {
	ref var m = ref *x.msg;
	WndUtil.PrintMsg(out var s, m.hwnd, m.message, m.wParam, m.lParam);
	print.it(s, x.sentByOtherThread);
});
dialog.show("hook");
```