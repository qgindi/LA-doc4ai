# Method `Au.clipboardData.getText`

Gets text from the clipboard.

```
public static string getText(int format = 13)
```

##### Parameters

- *format*  (`int`):
    Clipboard format id. Default: `Au.Types.ClipFormats.Text` (`CF_UNICODETEXT`). If 0, tries to get text (`Au.Types.ClipFormats.Text`) or file paths (`Au.Types.ClipFormats.Files`; returns multiline text). Text encoding depends on *format*; default UTF-16. See `Au.Types.ClipFormats.Register`.

##### Returns

`string`

`null` if there is no text.

##### Exceptions

- `Au.Types.AuException`:
    Failed to open clipboard (after 10 s of wait/retry).