# Method `Au.Triggers.AutotextTriggerArgs.Confirm`

Shows a 1-item menu below the text cursor (caret) or mouse cursor.

```
public bool Confirm(string text = "Replace")
```

##### Parameters

- *text*  (`string`):
    Text to display. This function limits it to 300 characters. Default: `"Replace"`.

##### Returns

`bool`

Returns `true` if the user clicked the item or pressed `Enter` or `Tab`.

#### Remarks

This function is used by `Au.Triggers.AutotextTriggerArgs.Replace` when used flag `Au.Triggers.TAFlags.Confirm`.

The user can close the menu with `Enter`, `Tab` or `Esc`. Other keys close the menu and are passed to the active window.

#### Examples

Code in file `Autotext triggers`.

```
//var tt = Triggers.Autotext;
tt["con1", TAFlags.Confirm] = o => o.Replace("Flag Confirm");
tt["con2"] = o => { if(o.Confirm("Example")) o.Replace("Function Confirm"); };
```

### See Also

`Au.Triggers.AutotextTriggers.MenuOptions`

`Au.popupMenu.defaultFont`

`Au.popupMenu.defaultMetrics`