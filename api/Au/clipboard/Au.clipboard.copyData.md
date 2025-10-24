# Method `Au.clipboard.copyData`

Gets data of any formats from the focused app using the clipboard and a callback function.

```
public static T copyData<T>(Func<T> callback, bool cut = false, OKey options = null, KHotkey hotkey = default, int timeoutMS = 0)
```

##### Parameters

- *callback*  (`Func<T>`):
    Callback function. It can get clipboard data of any formats. It can use any clipboard functions, for example `Au.clipboardData` or `System.Windows.Forms.Clipboard`. Don't call copy/paste functions.
- *cut*  (`bool`):
    Use `Ctrl+X`.
- *options*  (`Au.Types.OKey`):
    Options. If `null` (default), uses `Au.opt.key`. Uses `Au.Types.OKey.RestoreClipboard`, `Au.Types.OKey.KeySpeedClipboard`, `Au.Types.OKey.NoBlockInput`. Does not use `Au.Types.OKey.Hook`.
- *hotkey*  (`Au.Types.KHotkey`):
    Keys to use instead of `Ctrl+C` or `Ctrl+X`. Example: `hotkey: "Ctrl+Shift+C"`. Overrides *cut*.
- *timeoutMS*  (`int`):
    Max time to wait until the focused app sets clipboard data, in milliseconds. If 0 (default), the timeout is 3000 ms. The function waits up to 10 times longer if the window is hung.

##### Returns

`T`

The return value of *callback*.

##### Exceptions

- `Au.Types.AuException`:
    Failed. Fails if there is no focused window or if it does not set clipboard data.
- `Au.Types.InputDesktopException`

##### Type Parameters

- `T`

#### Remarks

Sends keys `Ctrl+C`, waits until the focused app sets clipboard data, calls the callback function that gets it, finally restores clipboard data. Fails if the focused app does not set clipboard data. Works with console windows too, even if they don't support `Ctrl+C`.

#### Examples

```
var image = clipboard.copyData(() => clipboardData.getImage());

var (text, files) = clipboard.copyData(() => (clipboardData.getText(), clipboardData.getFiles()));
```