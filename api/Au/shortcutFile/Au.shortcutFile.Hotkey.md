# Property `Au.shortcutFile.Hotkey`

Gets or sets hotkey.

```
public (KMod, KKey) Hotkey { get; set; }
```

##### Exceptions

- `ArgumentException`:
    The value for the `set` function includes `Win`.
- `Au.Types.AuException`:
    The `set` function failed.

##### Property Value

`(KMod, KKey)`