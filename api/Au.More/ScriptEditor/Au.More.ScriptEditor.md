# Class `Au.More.ScriptEditor`

Contains functions to interact with the script editor, if available.

```
public static class ScriptEditor
```

##### Remarks

Functions of this class work when editor process is running, even if current process wasn't started from it. To detect whether current process was started from editor, use `Au.folders.Editor` (it is `null` if not).

##### Inheritance

`object` → `ScriptEditor`

### Properties

`Available`, `IsPortable`

### Methods

`GetCommandState`, `GetFileInfo`, `GetFileInfo`, `GetIcon`, `InvokeCommand`, `MainWindow`, `Open`, `ShowMainWindow`, `TestCurrentFileInProject`