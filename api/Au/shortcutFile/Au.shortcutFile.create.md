# Method `Au.shortcutFile.create`

Creates a new `Au.shortcutFile` instance that can be used to create or replace a shortcut file.

```
public static shortcutFile create(string lnkPath)
```

##### Parameters

- *lnkPath*  (`string`):
    Shortcut file (`.lnk`) path.

##### Returns

`Au.shortcutFile`

##### Exceptions

- `ArgumentException`:
    Not full path.

#### Remarks

You can set properties and finally call `Au.shortcutFile.Save`. If the shortcut file already exists, `Save` replaces it.