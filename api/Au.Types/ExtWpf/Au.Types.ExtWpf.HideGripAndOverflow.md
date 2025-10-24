# Method `Au.Types.ExtWpf.HideGripAndOverflow`

Hides the grip and/or overflow controls in this toolbar. Call before the toolbar is loaded.

```
public static void HideGripAndOverflow(this ToolBar t, bool hideGrip = true, bool hideOverflow = true)
```

##### Parameters

- *t*  (`ToolBar`)
- *hideGrip*  (`bool`):
    Hide grip. Sets `SetIsLocked` `true`.
- *hideOverflow*  (`bool`):
    Hides the overflow button while it is disabled.

##### Exceptions

- `InvalidOperationException`:
    Loaded.