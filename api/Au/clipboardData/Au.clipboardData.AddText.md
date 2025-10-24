# Method `Au.clipboardData.AddText`

Adds text.

```
public clipboardData AddText(string text, int format = 13)
```

##### Parameters

- *text*  (`string`):
    Text.
- *format*  (`int`):
    Clipboard format id. Default: `Au.Types.ClipFormats.Text` (`CF_UNICODETEXT`). Text encoding depends on *format*; default UTF-16. See `Au.Types.ClipFormats.Register`.

##### Returns

`Au.clipboardData`

this.

##### Exceptions

- `ArgumentNullException`
- `ArgumentException`:
    Invalid *format*.
- `Exception`:
    Exceptions of `System.Text.Encoding.GetBytes`, which is called if encoding is not UTF-16.