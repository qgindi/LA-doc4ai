# Method `Au.folders.getFolder`

Gets path of a known folder by its name.

```
public static FolderPath getFolder(string folderName)
```

##### Parameters

- *folderName*  (`string`):

    Can be:

    - name of a property of this class, like `"Documents"`, `"Temp"`, `"ThisApp"`. The property must return `Au.Types.FolderPath` or `string`.
    - name of a property of the nested class `Au.folders.shell`, like `"shell.ControlPanel"`. Gets `":: ITEMIDLIST"`.
    - known folder canonical name. See `Au.folders.getKnownFolders`. If has prefix `"shell."`, gets `":: ITEMIDLIST"`. Much slower, but allows to get paths of folders registered by applications.

##### Returns

`Au.Types.FolderPath`

`null` if unavailable.

### See Also

`Au.pathname.expand`