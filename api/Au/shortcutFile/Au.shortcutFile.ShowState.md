# Property `Au.shortcutFile.ShowState`

Gets or sets the window show state. Most programs ignore it.

```
public int ShowState { get; set; }
```

##### Exceptions

- `Au.Types.AuException`:
    The `set` function failed.

##### Property Value

`int`

1 (normal, default), 2 (minimized) or 3 (maximized).