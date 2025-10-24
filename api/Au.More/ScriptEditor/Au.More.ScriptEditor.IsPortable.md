# Property `Au.More.ScriptEditor.IsPortable`

Returns `true` if the editor program is installed as [portable](../editor/Portable%20app.html).

```
public static bool IsPortable { get; }
```

##### Property Value

`bool`

#### Remarks

Available in the script editor process and in scripts launched from it. Elsewhere `false`.

If portable, these paths are different:

- `Au.folders.ThisAppDocuments`
- `Au.folders.ThisAppDataLocal`
- `Au.folders.ThisAppTemp`
- `Au.folders.Editor`
- `Au.folders.Workspace`