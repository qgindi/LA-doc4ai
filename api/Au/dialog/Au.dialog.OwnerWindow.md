# Method `Au.dialog.OwnerWindow`

Sets owner window.

```
public dialog OwnerWindow(AnyWnd owner, bool ownerCenter = false, bool dontDisable = false)
```

##### Parameters

- *owner*  (`Au.Types.AnyWnd`):
    Owner window, or one of its child/descendant controls. Can be `Au.wnd`, WPF window or element, winforms window or control. Can be `null`.
- *ownerCenter*  (`bool`):
    Show the dialog in the center of the owner window.
- *dontDisable*  (`bool`):
    Don't disable the owner window. If `false`, disables if it belongs to this thread.

##### Returns

`Au.dialog`

#### Remarks

The owner window will be disabled, and this dialog will be on top of it. This window will be in owner's screen, if screen was not explicitly specified (see `Au.dialog.InScreen`). `Au.dialog.options.defaultScreen` is ignored.

### See Also

`Au.dialog.options.autoOwnerWindow`