# Method `Au.More.RegisteredHotkey.Register`

Registers a hotkey using API `RegisterHotKey`.

```
public bool Register(int id, KHotkey hotkey, AnyWnd window = default, bool noRepeat = false)
```

##### Parameters

- *id*  (`int`):
    Hotkey id. Must be 0 to 0xBFFF or value returned by API `GlobalAddAtom`. It will be *wParam* of the `WM_HOTKEY` message.
- *hotkey*  (`Au.Types.KHotkey`):
    Hotkey. Can be: string like `"Ctrl+Shift+Alt+Win+K"`, tuple `(KMod, KKey)`, enum `Au.Types.KKey`, enum `Keys`, struct `Au.Types.KHotkey`.
- *window*  (`Au.Types.AnyWnd`):
    Window/form that will receive the `WM_HOTKEY` message. Must be of this thread. If default, the message must be retrieved in the message loop of this thread.
- *noRepeat*  (`bool`):
    Add flag `MOD_NOREPEAT`.

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.

##### Exceptions

- `ArgumentException`:
    Error in hotkey string.
- `InvalidOperationException`:
    This variable already registered a hotkey.

#### Remarks

Fails if the hotkey is currently registered by this or another application or used by Windows. Also if `F12`.

> **Note:**
> Most single-key and `Shift+key` hotkeys don't work when the active window has higher UAC integrity level (eg admin) than this process. Media keys may work.

A single variable cannot register multiple hotkeys simultaneously. Use multiple variables, for example array.

### See Also

`Au.keys.waitForHotkey`