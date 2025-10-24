# Method `Au.Types.ClipFormats.Register`

Registers a clipboard format and returns its id. If already registered, just returns id.

```
public static int Register(string name, Encoding textEncoding = null)
```

##### Parameters

- *name*  (`string`):
    Format name.
- *textEncoding*  (`Encoding`):
    Text encoding, if it's a text format. Used by `Au.clipboardData.getText`, `Au.clipboardData.AddText` and functions that call them. For example `System.Text.Encoding.UTF8`. If `null`, text of unknown formats is considered Unicode UTF-16 (no encoding/decoding needed).

##### Returns

`int`

#### Remarks

Calls API `RegisterClipboardFormat`.