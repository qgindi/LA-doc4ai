# Property `Au.shortcutFile.TargetPidl`

Gets or sets a non-file-system target (eg Control Panel) through its `ITEMIDLIST`.

```
public Pidl TargetPidl { get; set; }
```

##### Exceptions

- `Au.Types.AuException`:
    The `set` function failed.

##### Property Value

`Au.Types.Pidl`

#### Remarks

Also can be used for any target type, but gets raw value, for example MSI shortcut target is incorrect. Most but not all shortcuts have this property; the `get` function returns `null` if the shortcut does not have it.