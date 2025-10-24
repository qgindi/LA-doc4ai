# Method `Au.More.ScriptEditor.InvokeCommand`

Invokes an editor's menu command.

```
public static void InvokeCommand(string command, bool? check = null, bool dontWait = false, bool activateWindow = true)
```

##### Parameters

- *command*  (`string`):
    Command name. If `""` or invalid, prints all names.
- *check*  (`bool?`):
    If it's a checkbox-item, `true` checks it, `false` unchecks, `null` toggles. Else must be `null` (default).
- *dontWait*  (`bool`):
    Don't wait until the command finishes executing. For example, if it shows a modal dialog, don't wait until it is closed.
- *activateWindow*  (`bool`):
    Activate the main window. Default `true`. Some commands may not work correctly if the window isn't active.

#### Remarks

Shows the main window, regardless of *activateWindow*. Waits while it is disabled or not finished loading, unless script role is `editorExtension` and it runs in the editor's main thread (then not invoke the command). Does not invoke the command if the menu item is disabled or if it's a submenu-item.