# Method `Au.clipboard.copy`

Gets the selected text from the focused app using the clipboard.

```
public static string copy(bool cut = false, OKey options = null, KHotkey hotkey = default, int timeoutMS = 0)
```

##### Parameters

- *cut*  (`bool`):
    Use `Ctrl+X`.
- *options*  (`Au.Types.OKey`):
    Options. If `null` (default), uses `Au.opt.key`. Uses `Au.Types.OKey.RestoreClipboard`, `Au.Types.OKey.KeySpeedClipboard`, `Au.Types.OKey.NoBlockInput`. Does not use `Au.Types.OKey.Hook`.
- *hotkey*  (`Au.Types.KHotkey`):
    Keys to use instead of `Ctrl+C` or `Ctrl+X`. Example: `hotkey: "Ctrl+Shift+C"`. Overrides *cut*.
- *timeoutMS*  (`int`):
    Max time to wait until the focused app sets clipboard data, in milliseconds. If 0 (default), the timeout is 3000 ms. The function waits up to 10 times longer if the window is hung.

##### Returns

`string`

##### Exceptions

- `Au.Types.AuException`:
    Failed. Fails if there is no focused window or if it does not set clipboard data.
- `Au.Types.InputDesktopException`

#### Remarks

Also can get file paths, as multiline text.

Sends keys `Ctrl+C`, waits until the focused app sets clipboard data, gets it, finally restores clipboard data. Fails if the focused app does not set clipboard text or file paths, for example if there is no selected text/files. Works with console windows too, even if they don't support `Ctrl+C`.