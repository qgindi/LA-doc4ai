# Property `Au.folders.ThisAppDataLocal`

Gets or sets path of folder "local (non-roaming) private files of this application of this user account".

```
public static FolderPath ThisAppDataLocal { get; set; }
```

##### Exceptions

- `InvalidOperationException`:
    Thrown by the `set` function if this property is already set.

##### Property Value

`Au.Types.FolderPath`

#### Remarks

Default path depends on script role (`Au.script.role` and portable mode (`Au.More.ScriptEditor.IsPortable`):

- `miniProgram` and `exeProgram` - `folders.LocalAppData + @"LibreAutomate\_script"`. Or `folders.LocalAppData + "Au"`, if exists (for backward compatibility).
- `editorExtension` - `folders.LocalAppData + "LibreAutomate"`. Cannot be changed.
- Portable `miniProgram` and `exeProgram` - `folders.ThisApp + @"data\appLocal\_script"`. Note: `exeProgram` launched not from editor isn't portable.
- Portable `editorExtension` - `folders.ThisApp + @"data\appLocal"`. Cannot be changed.

The `set` function does not change system settings. It just remembers a string that will be later returned by the `get` function in this process. Creates the folder if does not exist when `set` or `get` function called first time in this process, unless `Au.folders.noAutoCreate` `true`.