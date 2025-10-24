# Property `Au.folders.ThisAppDataCommon`

Gets or sets path of folder "common (all users) private files of this application".

```
public static FolderPath ThisAppDataCommon { get; set; }
```

##### Exceptions

- `InvalidOperationException`:
    Thrown by the `set` function if this property is already set.

##### Property Value

`Au.Types.FolderPath`

#### Remarks

Default path depends on script role (`Au.script.role` and portable mode (`Au.More.ScriptEditor.IsPortable`):

- `miniProgram` and `exeProgram` - `folders.ProgramData + @"LibreAutomate\_script"`. Or `folders.ProgramData + "Au"`, if exists (for backward compatibility).
- `editorExtension` - `folders.ProgramData + "LibreAutomate"`. Cannot be changed.
- Portable `miniProgram` and `exeProgram` - `folders.ThisApp + @"data\appCommon\_script"`. Note: `exeProgram` launched not from editor isn't portable.
- Portable `editorExtension` - `folders.ThisApp + @"data\appCommon"`. Cannot be changed.

The `set` function does not change system settings. It just remembers a string that will be later returned by the `get` function in this process. This function does not auto-create the folder; usually it is created when installing the application; the script editor does not use and does not install it. Note: the `ProgramData` folder has special security permissions. Programs running not as administrator usually cannot write there, unless your installer changed folder security permissions.