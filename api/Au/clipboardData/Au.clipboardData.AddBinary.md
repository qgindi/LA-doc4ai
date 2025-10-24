# Method `Au.clipboardData.AddBinary`

Adds data of any format as `byte[]`.

```
public clipboardData AddBinary(byte[] data, int format)
```

##### Parameters

- *data*  (`byte[]`):
    `byte[]` containing data.
- *format*  (`int`):
    Clipboard format id. See `Au.Types.ClipFormats.Register`.

##### Returns

`Au.clipboardData`

this.

##### Exceptions

- `ArgumentNullException`
- `ArgumentException`:
    Invalid *format*. Supported are all registered formats and standard formats `<CF_MAX` except GDI handles.