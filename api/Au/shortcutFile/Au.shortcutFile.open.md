# Method `Au.shortcutFile.open`

Opens a shortcut file (`.lnk`) for getting shortcut properties.

```
public static shortcutFile open(string lnkPath)
```

##### Parameters

- *lnkPath*  (`string`):
    Shortcut file (`.lnk`) path.

##### Returns

`Au.shortcutFile`

##### Exceptions

- `ArgumentException`:
    Not full path.
- `Au.Types.AuException`:
    Failed to open `.lnk` file.