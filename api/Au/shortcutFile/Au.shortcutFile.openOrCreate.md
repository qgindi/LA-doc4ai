# Method `Au.shortcutFile.openOrCreate`

Creates a new `Au.shortcutFile` instance that can be used to create or modify a shortcut file.

```
public static shortcutFile openOrCreate(string lnkPath)
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
    Failed to open existing `.lnk` file.

#### Remarks

Exception if file exists but cannot open it for read-write access. You can get and set properties and finally call `Au.shortcutFile.Save`. If the shortcut file already exists, `Save` updates it.