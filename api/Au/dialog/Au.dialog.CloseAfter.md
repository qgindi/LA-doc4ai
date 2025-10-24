# Method `Au.dialog.CloseAfter`

Sets to automatically close the dialog after *timeoutS* seconds. Then `Au.dialog.ShowDialog` returns `Au.dialog.Timeout`.

```
public dialog CloseAfter(int timeoutS, string timeoutAction = null, bool noInfo = false)
```

##### Parameters

- *timeoutS*  (`int`):
    Timeout in seconds.
- *timeoutAction*  (`string`):
    Short text to display what will happen on timeout. For example button name. See `Au.dialog.options.timeoutTextFormat`.
- *noInfo*  (`bool`):
    Don't display the timeout information in the footer.

##### Returns

`Au.dialog`