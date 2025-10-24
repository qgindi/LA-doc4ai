# Method `Au.clipboard.pasteData`

Pastes data added to a `Au.clipboardData` variable into the focused app using the clipboard.

```
public static void pasteData(clipboardData data, OKey options = null, KHotkey hotkey = default, int timeoutMS = 0)
```

##### Parameters

- *data*  (`Au.clipboardData`)
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

Paste data of two formats: HTML and text.

```
clipboard.pasteData(new clipboardData().AddHtml("<b>text</b>").AddText("text"));
```

### See Also

`Au.keys.sendt`