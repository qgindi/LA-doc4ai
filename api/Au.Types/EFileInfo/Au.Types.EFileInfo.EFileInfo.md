# Constructor of `Au.Types.EFileInfo`

```
public EFileInfo(string name, string path, string text, EFileKind kind, uint id, string filePath, string workspace)
```

##### Parameters

- *name*  (`string`):
    File name, like `"File.cs"`.
- *path*  (`string`):
    Path in workspace, like `@"\Folder\File.cs"`.
- *text*  (`string`):
    File text; null if *needText* false or if failed to get text. If the file is open in editor, it's the editor text, else it's the saved text.
- *kind*  (`Au.Types.EFileKind`)
- *id*  (`uint`):
    File id.
- *filePath*  (`string`):
    Full path.
- *workspace*  (`string`):
    Path of the workspace folder.