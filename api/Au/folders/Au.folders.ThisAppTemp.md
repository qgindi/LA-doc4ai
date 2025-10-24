# Property `Au.folders.ThisAppTemp`

Gets or sets path of folder "temporary files of this application".

```
public static FolderPath ThisAppTemp { get; set; }
```

##### Exceptions

- `InvalidOperationException`:
    Thrown by the `set` function if this property is already set.

##### Property Value

`Au.Types.FolderPath`

#### Remarks

Default path depends on script role (`Au.script.role` and portable mode (`Au.More.ScriptEditor.IsPortable`):

- `miniProgram` and `exeProgram` - `folders.Temp + @"LibreAutomate\_script"`. Or `folders.Temp + "Au"`, if exists (for backward compatibility).
- `editorExtension` - `folders.Temp + "LibreAutomate"`. Cannot be changed.
- Portable `miniProgram` and `exeProgram` - `folders.ThisApp + @"data\temp\_script"`. Note: `exeProgram` launched not from editor isn't portable.
- Portable `editorExtension` - `folders.ThisApp + @"data\temp"`. Cannot be changed.

The `set` function does not change system settings. It just remembers a string that will be later returned by the `get` function in this process. Creates the folder if does not exist when `set` or `get` function called first time in this process, unless `Au.folders.noAutoCreate` `true`.