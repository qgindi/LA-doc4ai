# Method `Au.shortcutFile.GetIconLocation`

Gets custom icon file path and icon index.

```
public string GetIconLocation(out int iconIndex)
```

##### Parameters

- *iconIndex*  (`int`):
    Receives 0 or icon index or negative icon resource id.

##### Returns

`string`

`null` if the shortcut does not have a custom icon (then you see its target icon).