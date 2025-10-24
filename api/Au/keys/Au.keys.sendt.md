# Method `Au.keys.sendt`

Sends text to the active window, using virtual keystrokes or clipboard.

```
public static void sendt(string text, string html = null)
```

##### Parameters

- *text*  (`string`):
    Text. Can be `null`.
- *html*  (`string`):
    HTML. Can be full HTML or fragment. See `Au.clipboardData.AddHtml`. Can be specified only *text* or only *html* or both. If both, will paste *html* in apps that support it, elsewhere *text*. If only *html*, in apps that don't support HTML will paste *html* as text.

##### Exceptions

- `Au.Types.AuException`:
    Failed. Fails if there is no focused window.
- `Au.Types.InputDesktopException`

#### Remarks

Calls `Au.keys.AddText` and `Au.keys.SendNow`. To send text can use keys, characters or clipboard, depending on `Au.opt.key` and text. If *html* not `null`, uses clipboard.

#### Examples

```
keys.sendt("Text.\r\n");
```

Or use function `Au.keys.send` and prefix `"!"`. For HTML use prefix `"%"`.

```
keys.send("!Send this text and press key", "Enter");
keys.send("%<b>bold</b> <i>italic</i>", "Enter");
```

### See Also

`Au.clipboard.paste`