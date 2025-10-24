# Method `Au.More.WindowsHook.Mouse`

Sets a low-level mouse hook (`WH_MOUSE_LL`). See API `SetWindowsHookEx`.

```
public static WindowsHook Mouse(Action<HookData.Mouse> hookProc, bool ignoreAuInjected = true, bool setNow = true)
```

##### Parameters

- *hookProc*  (`Action<Au.Types.HookData.Au.Types.HookData.Mouse>`):

    The hook procedure (function that handles hook events). Must return as soon as possible. More info: `Au.More.WindowsHook.LowLevelHooksTimeout`. If calls `Au.Types.HookData.Mouse.BlockEvent` or `Au.Types.HookData.ReplyMessage(true)`, the event is not sent to apps and other hooks. Event data cannot be modified.

    > **Note:**
    >     When the hook procedure returns, the parameter variable becomes invalid and unsafe to use. If you need the data for later use, copy its properties and not whole variable.
- *ignoreAuInjected*  (`bool`):
    Don't call the hook procedure for events sent by functions of this library. Default `true`.
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
var stop = false;
using var hook = WindowsHook.Mouse(x => {
	print.it(x);
	if(x.Event == HookData.MouseEvent.RightButton) { stop = x.IsButtonUp; x.BlockEvent(); }
});
dialog.show("hook");
//or
//wait.doEventsUntil(-10, () => stop); //wait max 10 s for right-click
//print.it("the end");
```