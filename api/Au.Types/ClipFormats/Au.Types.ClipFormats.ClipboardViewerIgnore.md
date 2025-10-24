# Property `Au.Types.ClipFormats.ClipboardViewerIgnore`

Registered format `"Clipboard Viewer Ignore"`.

```
public static int ClipboardViewerIgnore { get; }
```

##### Property Value

`int`

#### Remarks

Some clipboard viewer/manager programs don't try to get clipboard data if this format is present. For example Ditto, Clipdiary. The copy/paste functions of this library add this format to the clipboard to avoid displaying the temporary text/data in these programs, which also could make the paste function slower and less reliable.