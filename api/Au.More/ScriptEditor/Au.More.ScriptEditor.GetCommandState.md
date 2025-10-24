# Method `Au.More.ScriptEditor.GetCommandState`

Gets the state of an editor's menu command (checked, disabled).

```
public static ECommandState GetCommandState(string command)
```

##### Parameters

- *command*  (`string`):
    Command name. If `""` or invalid, prints all names.

##### Returns

`Au.Types.ECommandState`

#### Remarks

Shows the main window. Waits while it is disabled or not finished loading, unless script role is `editorExtension` and it runs in the editor's main thread (then returns `Disabled`).