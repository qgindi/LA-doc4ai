# Method `Au.clipboard.tryPaste`

Calls `Au.clipboard.paste` and handles exceptions.

```
public static bool tryPaste(string text, int timeout, bool warning = false, bool osd = false, string html = null, OKey options = null, KHotkey hotkey = default)
```

##### Parameters

- *text*  (`string`):
    Text. Can be `null` if *html* used.
- *timeout*  (`int`):
    Max time to wait until the focused app gets clipboard data, in milliseconds. The function waits up to 10 times longer if the window is hung.
- *warning*  (`bool`):
    Call `Au.print.warning`.
- *osd*  (`bool`):
    Call `Au.osdText.showTransparentText` with text `"Failed to paste text"`.
- *html*  (`string`):
    HTML. Can be full HTML or fragment. See `Au.clipboardData.AddHtml`. Can be `null`. Can be specified only *text* or only *html* or both. If both, will paste *html* in apps that support it, elsewhere *text*. If only *html*, in apps that don't support HTML will paste *html* as text.
- *options*  (`Au.Types.OKey`):
    Options. If `null` (default), uses `Au.opt.key`. Uses `Au.Types.OKey.PasteSleep`, `Au.Types.OKey.RestoreClipboard`, `Au.Types.OKey.PasteWorkaround`, `Au.Types.OKey.KeySpeedClipboard`, `Au.Types.OKey.NoBlockInput`, `Au.Types.OKey.Hook`.
- *hotkey*  (`Au.Types.KHotkey`):
    Keys to use instead of `Ctrl+V`. Example: `hotkey: "Ctrl+Shift+V"`.

##### Returns

`bool`

Returns `false` if failed.

#### Remarks

Sets clipboard data, sends keys `Ctrl+V`, waits until the focused app gets clipboard data, finally restores clipboard data. Fails if nothing gets clipboard data in several seconds. Works with console windows too, even if they don't support `Ctrl+V`.

A clipboard viewer/manager program can make this function slower and less reliable, unless it supports `Au.Types.ClipFormats.ClipboardViewerIgnore` or gets clipboard data with a delay. Possible problems with some virtual PC programs. Either pasting does not work in their windows, or they use a hidden clipboard viewer that makes this function slower and less reliable.