# Method `Au.clipboard.tryCopy`

Calls `Au.clipboard.copy` and handles exceptions.

```
public static bool tryCopy(out string text, int timeout, bool warning = false, bool osd = false, OKey options = null, KHotkey hotkey = default)
```

##### Parameters

- *text*  (`string`):
    Receives the copied text.
- *timeout*  (`int`):
    Max time to wait until the focused app sets clipboard data, in milliseconds. The function waits up to 10 times longer if the window is hung.
- *warning*  (`bool`):
    Call `Au.print.warning`.
- *osd*  (`bool`):
    Call `Au.osdText.showTransparentText` with text `"Failed to copy text"`.
- *options*  (`Au.Types.OKey`):
    Options. If `null` (default), uses `Au.opt.key`. Uses `Au.Types.OKey.RestoreClipboard`, `Au.Types.OKey.KeySpeedClipboard`, `Au.Types.OKey.NoBlockInput`. Does not use `Au.Types.OKey.Hook`.
- *hotkey*  (`Au.Types.KHotkey`):
    Keys to use instead of `Ctrl+C` or `Ctrl+X`. Example: `hotkey: "Ctrl+Shift+C"`. Overrides *cut*.

##### Returns

`bool`

Returns `false` if failed.

#### Remarks

Also can get file paths, as multiline text.

Sends keys `Ctrl+C`, waits until the focused app sets clipboard data, gets it, finally restores clipboard data. Fails if the focused app does not set clipboard text or file paths, for example if there is no selected text/files. Works with console windows too, even if they don't support `Ctrl+C`.