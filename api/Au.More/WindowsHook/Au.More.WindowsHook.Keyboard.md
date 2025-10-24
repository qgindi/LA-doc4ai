# Method `Au.More.WindowsHook.Keyboard`

Sets a low-level keyboard hook (`WH_KEYBOARD_LL`). See API `SetWindowsHookEx`.

```
public static WindowsHook Keyboard(Action<HookData.Keyboard> hookProc, bool ignoreAuInjected = true, bool setNow = true)
```

##### Parameters

- *hookProc*  (`Action<Au.Types.HookData.Au.Types.HookData.Keyboard>`):

    The hook procedure (function that handles hook events). Must return as soon as possible. More info: `Au.More.WindowsHook.LowLevelHooksTimeout`. If calls `Au.Types.HookData.Keyboard.BlockEvent` or `Au.Types.HookData.ReplyMessage(true)`, the event is not sent to apps and other hooks. Event data cannot be modified.

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
using var hook = WindowsHook.Keyboard(x => {
	print.it(x);
	if(x.vkCode == KKey.Escape) { stop = true; x.BlockEvent(); }
});
dialog.show("hook");
//or
//wait.doEventsUntil(-10, () => stop); //wait max 10 s for Esc key
//print.it("the end");
```