# Method `Au.clipboardData.AddFiles`

Adds list of files to copy/paste. Uses clipboard format `Au.Types.ClipFormats.Files` (`CF_HDROP`).

```
public clipboardData AddFiles(params string[] files)
```

##### Parameters

- *files*  (`string[]`):
    One or more file paths.

##### Returns

`Au.clipboardData`

this.

##### Exceptions

- `ArgumentNullException`