# Constructor of `Au.More.TempFile`

Creates full path string with a unique filename (GUID) for a temporary file.

```
public TempFile(string ext = ".tmp", string directory = null)
```

##### Parameters

- *ext*  (`string`):
    Filename extension with dot. Default: `".tmp"`. Can be `null`.
- *directory*  (`string`):
    Parent directory. If `null` (default), uses `Au.folders.ThisAppTemp`. The function creates the directory if does not exist.

##### Exceptions

- `ArgumentException`:
    *directory* not full path.
- `Au.Types.AuException`:
    Failed to create directory.