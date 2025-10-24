# Property `Au.shortcutFile.TargetPath`

Gets or sets shortcut target path.

```
public string TargetPath { get; set; }
```

##### Exceptions

- `Au.Types.AuException`:
    The `set` function failed.
- `ArgumentException`:
    The `set` function allows max length 259.

##### Property Value

`string`

`null` if target isn't a file system object, eg Control Panel or URL.

#### Remarks

The `get` function gets path with expanded environment variables. If possible, it corrects the target of MSI shortcuts and 64-bit Program Files shortcuts where `IShellLink.GetPath` lies.