# Property `Au.shortcutFile.TargetURL`

Gets or sets a URL target. Note: it is a `.lnk` shortcut, not a `.url` shortcut.

```
public string TargetURL { get; set; }
```

##### Exceptions

- `Au.Types.AuException`:
    The `set` function failed.

##### Property Value

`string`

The `get` function returns string `"file:///..."` if target is a file.