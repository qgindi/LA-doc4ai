# Property `Au.More.FileOpenSaveDialog.InitFolderNow`

Initial folder to use now. In most cases it's recommended to use `Au.More.FileOpenSaveDialog.InitFolderFirstTime` instead.

```
public string InitFolderNow { get; set; }
```

##### Property Value

`string`

#### Examples

```
d.InitFolderNow = @"C:\Test";
d.InitFolderNow = /* This PC */ ":: 14001f50e04fd020ea3a6910a2d808002b30309d";
```