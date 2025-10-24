# Method `Au.More.FileOpenSaveDialog.ShowOpen`

## Overload 1

Shows "Open" or "Select Folder" dialog that allows to select single item.

```
public bool ShowOpen(out string result, AnyWnd owner = default, bool selectFolder = false, bool onlyFilesystem = true, bool fileMustExist = true, bool previewPane = false)
```

##### Parameters

- *result*  (`string`):
    Full path of the selected file.
- *owner*  (`Au.Types.AnyWnd`):
    Owner window. Optional.
- *selectFolder*  (`bool`):
    Select folders, not files.
- *onlyFilesystem*  (`bool`):
    The dialog allows to select only file system items (files, folders), not other shell items or URLs. Default `true`. If `false`, other shell items are returned like `":: ITEMIDLIST"`; see `Au.Types.Pidl`.
- *fileMustExist*  (`bool`):
    The dialog can return only existing items. Default `true`.
- *previewPane*  (`bool`):
    Display the preview pane.

##### Returns

`bool`

`true` on **OK**, `false` on **Cancel** or error.

* * *

## Overload 2

Shows "Open" or "Select Folder" dialog that allows to select multiple items.

```
public bool ShowOpen(out string[] result, AnyWnd owner = default, bool selectFolder = false, bool onlyFilesystem = true, bool fileMustExist = true, bool previewPane = false)
```

##### Parameters

- *result*  (`string[]`):
    Full paths of the selected files.
- *owner*  (`Au.Types.AnyWnd`):
    Owner window. Optional.
- *selectFolder*  (`bool`):
    Select folders, not files.
- *onlyFilesystem*  (`bool`):
    The dialog allows to select only file system items (files, folders), not other shell items or URLs. Default `true`. If `false`, other shell items are returned like `":: ITEMIDLIST"`; see `Au.Types.Pidl`.
- *fileMustExist*  (`bool`):
    The dialog can return only existing items. Default `true`.
- *previewPane*  (`bool`):
    Display the preview pane.

##### Returns

`bool`

`true` on **OK**, `false` on **Cancel** or error.