# Method `Au.clipboard.paste`

Pastes text or HTML into the focused app using the clipboard.

```
public static void paste(string text, string html = null, OKey options = null, KHotkey hotkey = default, int timeoutMS = 0)
```

##### Parameters

- *text*  (`string`):
    Text. Can be `null` if *html* used.
- *html*  (`string`):
    HTML. Can be full HTML or fragment. See `Au.clipboardData.AddHtml`. Can be `null`. Can be specified only *text* or only *html* or both. If both, will paste *html* in apps that support it, elsewhere *text*. If only *html*, in apps that don't support HTML will paste *html* as text.
- *options*  (`Au.Types.OKey`):
    Options. If `null` (default), uses `Au.opt.key`. Uses `Au.Types.OKey.PasteSleep`, `Au.Types.OKey.RestoreClipboard`, `Au.Types.OKey.PasteWorkaround`, `Au.Types.OKey.KeySpeedClipboard`, `Au.Types.OKey.NoBlockInput`, `Au.Types.OKey.Hook`.
- *hotkey*  (`Au.Types.KHotkey`):
    Keys to use instead of `Ctrl+V`. Example: `hotkey: "Ctrl+Shift+V"`.
- *timeoutMS*  (`int`):
    Max time to wait until the focused app gets clipboard data, in milliseconds. If 0 (default), the timeout is 3000 ms. The function waits up to 10 times longer if the window is hung.

##### Exceptions

- `Au.Types.AuException`:
    Failed. Fails if there is no focused window or if it does not get clipboard data.
- `Au.Types.InputDesktopException`

#### Remarks

Sets clipboard data, sends keys `Ctrl+V`, waits until the focused app gets clipboard data, finally restores clipboard data. Fails if nothing gets clipboard data in several seconds. Works with console windows too, even if they don't support `Ctrl+V`.

A clipboard viewer/manager program can make this function slower and less reliable, unless it supports `Au.Types.ClipFormats.ClipboardViewerIgnore` or gets clipboard data with a delay. Possible problems with some virtual PC programs. Either pasting does not work in their windows, or they use a hidden clipboard viewer that makes this function slower and less reliable.

#### Examples

```
clipboard.paste("Example\r\n");
```

### See Also

`Au.keys.sendt`