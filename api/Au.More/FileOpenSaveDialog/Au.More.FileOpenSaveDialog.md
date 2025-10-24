# Class `Au.More.FileOpenSaveDialog`

Shows standard "Open", "Save As" or "Select Folder" dialog to select a file or folder.

```
public class FileOpenSaveDialog
```

##### Remarks

This class exists because the similar .NET classes have these problems:

- May disable the `System.AppDomain.UnhandledException` event.
- As owner window they support only `Window` or `Form`. This class also supports window handles.
- They support only filesystem items.
- There is no option to not add the selected file to recent files that are displayed in the context menu of the taskbar button etc.
- The WPF class does not have a client GUID property.

There are 2 main dialog types - open (`Au.More.FileOpenSaveDialog.ShowOpen`) and save (`Au.More.FileOpenSaveDialog.ShowSave`). All other functions of this class (properties, etc) are common to opening and saving.

##### Examples

```
var d = new FileOpenSaveDialog { FileTypes = "Text files|*.txt|All files|*.*" };
if(d.ShowOpen(out string s)) print.it(s);
```

##### Inheritance

`object` → `FileOpenSaveDialog`

### Constructors

`FileOpenSaveDialog(string, bool)`

### Properties

`CommonFlags`, `DefaultExt`, `FileNameLabel`, `FileNameText`, `FileTypeIndex`, `FileTypes`, `InitFolderFirstTime`, `InitFolderNow`, `OkButtonLabel`, `Title`

### Methods

`ShowOpen`, `ShowOpen`, `ShowSave`