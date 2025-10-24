# Method `Au.More.WindowsHook.ThreadGetMessage`

Sets a `WH_GETMESSAGE` hook for a thread of this process. See API `SetWindowsHookEx`.

```
public static WindowsHook ThreadGetMessage(Action<HookData.ThreadGetMessage> hookProc, int threadId = 0, bool setNow = true)
```

##### Parameters

- *hookProc*  (`Action<Au.Types.HookData.Au.Types.HookData.ThreadGetMessage>`):

    The hook procedure (function that handles hook events). Must return as soon as possible. The event cannot be canceled. As a workaround, you can set `msg->message=0`. Also can modify other fields.

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
using var hook = WindowsHook.ThreadGetMessage(x => {
	print.it(x.msg->ToString(), x.PM_NOREMOVE);
});
dialog.show("hook");
```