# Method `Au.dialog.RadioButtons`

Adds radio buttons.

```
public dialog RadioButtons(Strings buttons, int idDefault = 0)
```

##### Parameters

- *buttons*  (`Au.Types.Strings`):
    A list of strings `"id text"` separated by `|`, like `"1 One|2 Two|3 Three"`.
- *idDefault*  (`int`):
    Check the radio button that has this id. If omitted or 0, checks the first. If negative, does not check.

##### Returns

`Au.dialog`

#### Remarks

To get selected radio button id after closing the dialog, use `Au.dialog.Controls`.