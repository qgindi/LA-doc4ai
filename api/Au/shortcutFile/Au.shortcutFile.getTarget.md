# Method `Au.shortcutFile.getTarget`

Gets shortcut target path. It also can be a URL or a `ITEMIDLIST` string (see `Au.Types.Pidl`) of a virtual shell object. Uses `Au.shortcutFile.open` and `Au.shortcutFile.TargetAnyType`.

```
public static string getTarget(string lnkPath)
```

##### Parameters

- *lnkPath*  (`string`):
    Shortcut file (`.lnk`) path.

##### Returns

`string`

##### Exceptions

- `Au.Types.AuException`:
    Failed to open.