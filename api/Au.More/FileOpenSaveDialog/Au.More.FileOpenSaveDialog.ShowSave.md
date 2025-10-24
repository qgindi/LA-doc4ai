# Method `Au.More.FileOpenSaveDialog.ShowSave`

Shows "Save As" dialog.

```
public bool ShowSave(out string result, AnyWnd owner = default, bool overwritePrompt = true, string initFile = null)
```

##### Parameters

- *result*  (`string`):
    Full path of the selected file.
- *owner*  (`Au.Types.AnyWnd`):
    Owner window. Optional.
- *overwritePrompt*  (`bool`):
    If the selected file already exists, show a message box. Default `true`.
- *initFile*  (`string`):
    The initially selected file. Its name is displayed in the file name edit box, and the containing folder is opened. This would generally be used when the application is saving a file that already exists. For new files use `Au.More.FileOpenSaveDialog.FileNameText`.

##### Returns

`bool`

`true` on **OK**, `false` on **Cancel** or error.