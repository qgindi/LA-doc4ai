# Method `Au.More.ScriptEditor.GetFileInfo`

## Overload 1

Gets name, text and some info of the currently active file in editor.

```
public static EFileInfo GetFileInfo(bool needText)
```

##### Parameters

- *needText*  (`bool`):
    Need text too.

##### Returns

`Au.Types.EFileInfo`

`null` if there are no open files or if failed.

* * *

## Overload 2

Gets name, text and some info of a file in the current workspace in editor.

```
public static EFileInfo GetFileInfo(string file, bool needText)
```

##### Parameters

- *file*  (`string`):
    A file in current workspace. Can be full path, or relative path in workspace, or file name with extension (`".cs"` etc), or `":id"`.
- *needText*  (`bool`):
    Need text too.

##### Returns

`Au.Types.EFileInfo`

`null` if the specified file not found or if failed.