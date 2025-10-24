# Method `Au.wpfBuilder.LoadFile`

Loads a web page or RTF text from a file or URL into the last added element.

```
public wpfBuilder LoadFile(string source)
```

##### Parameters

- *source*  (`string`):
    File or URL to load. Supported element types and sources: `System.Windows.Controls.WebBrowser`, `System.Windows.Controls.Frame` - URL or file path. `System.Windows.Controls.RichTextBox` - path of a local `.rtf` file.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:

    - Unsupported element type.
    - `System.Windows.Controls.RichTextBox` *source* does not end with `".rtf"`.

#### Remarks

If fails to load, prints warning. See `Au.print.warning`.