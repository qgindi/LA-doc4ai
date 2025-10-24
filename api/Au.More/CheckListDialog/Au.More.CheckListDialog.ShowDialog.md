# Method `Au.More.CheckListDialog.ShowDialog`

Adds **OK**/**Cancel** buttons, shows dialog, sets result properties.

```
public bool ShowDialog(DependencyObject owner = null)
```

##### Parameters

- *owner*  (`DependencyObject`):
    Owner window, or an element in it. If used, sets `System.Windows.Window.ShowInTaskbar` = `false`. Else sets `System.Windows.Window.Topmost` = `true`, unless `Au.dialog.options.topmostIfNoOwnerWindow` is `false` or the active window belongs to this process.

##### Returns

`bool`

`true` if pressed **OK**.