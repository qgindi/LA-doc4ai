# Constructor of `Au.More.CheckListDialog`

Creates `Au.More.CheckListDialog.Builder`, sets some window properties, optionally sets static text.

```
public CheckListDialog(string text = null, string title = null)
```

##### Parameters

- *text*  (`string`):
    Text above the list. Can be `null`. See also `Au.More.CheckListDialog.FormatText`.
- *title*  (`string`):
    Window name. If `null`, uses `Au.dialog.options.defaultTitle`.