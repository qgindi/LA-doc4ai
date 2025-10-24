# Method `Au.More.WindowsHook.ThreadKeyboard`

Sets a `WH_GETMESSAGE` hook for a thread of this process. See API `SetWindowsHookEx`.

```
public static WindowsHook ThreadKeyboard(Func<HookData.ThreadKeyboard, bool> hookProc, int threadId = 0, bool setNow = true)
```

##### Parameters

- *hookProc*  (`Func<Au.Types.HookData.Au.Types.HookData.ThreadKeyboard, bool>`):
    The hook procedure (function that handles hook events). Must return as soon as possible. If returns `true`, the event is canceled.
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
using var hook = WindowsHook.ThreadKeyboard(x => {
	print.it(x.key, 0 != (x.lParam & 0x80000000) ? "up" : "", x.lParam, x.PM_NOREMOVE);
	return false;
});
dialog.show("hook");
```