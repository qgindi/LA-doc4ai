# Method `Au.clipboardData.getFiles`

Gets file paths from the clipboard. Uses clipboard format `Au.Types.ClipFormats.Files` (`CF_HDROP`).

```
public static string[] getFiles()
```

##### Returns

`string[]`

`null` if there is no data of this format.

##### Exceptions

- `Au.Types.AuException`:
    Failed to open clipboard (after 10 s of wait/retry).