# Method `Au.toolbar.getSettingsFilePath`

Gets full path of toolbar's settings file. The file may exist or not.

```
public static string getSettingsFilePath(string toolbarName)
```

##### Parameters

- *toolbarName*  (`string`):
    Toolbar name. If this string is a full path, returns this string.

##### Returns

`string`

#### Remarks

Path: `folders.Workspace + $@"\.toolbars\{toolbarName}.json"`. If `Au.folders.Workspace` is `null`, uses `Au.folders.ThisAppDataRoaming`.