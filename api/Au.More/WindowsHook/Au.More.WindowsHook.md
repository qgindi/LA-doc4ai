# Class `Au.More.WindowsHook`

Wraps API `SetWindowsHookEx`.

```
public sealed class WindowsHook : IDisposable
```

##### Remarks

Hooks are used to receive notifications about various system events. Keyboard and mouse input, window messages, various window events.

Threads that use hooks must process Windows messages. For example have a window/dialog/messagebox, or use a "wait-for" function that dispatches messages or has such option (see `Au.Types.Seconds.DoEvents`).

> **Important:**
> The variable should be disposed when don't need, or at least unhooked, either explicitly (call `Au.More.WindowsHook.Dispose` or `Au.More.WindowsHook.Unhook` in same thread) or with `using`. Can do it in hook procedure.

> **Warning:**
> Avoid many hooks. Each low-level keyboard or mouse hook makes the computer slower, even if the hook procedure is fast. On each input event (key down, key up, mouse move, click, wheel) Windows sends a message to your thread.

To receive hook events is used a callback function, aka hook procedure. Hook procedures of some hook types can block some events (call `Au.Types.HookData.Keyboard.BlockEvent` or return `true`). Blocked events are not sent to apps and older hooks.

Delegates of hook procedures are protected from GC until called `Au.More.WindowsHook.Dispose` or until the thread ends, even of unreferenced `WindowsHook` variables.

UI element functions may fail in hook procedures of low-level keyboard and mouse hooks. Workarounds exist.

Exists an alternative way to monitor keyboard or mouse events - raw input API. Good: less overhead; can detect from which device the input event came. Bad: cannot block events; incompatible with low-level keyboard hooks. This library does not have functions to make the API easier to use.

##### Inheritance

`object` → `WindowsHook`

### Properties

`IsSet`, `LowLevelHooksTimeout`

### Methods

`Dispose`, `Hook`, `Keyboard`, `Mouse`, `Restore`, `ThreadCallWndProc`, `ThreadCallWndProcRet`, `ThreadCbt`, `ThreadGetMessage`, `ThreadKeyboard`, `ThreadMouse`, `Unhook`