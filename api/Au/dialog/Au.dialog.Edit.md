# Method `Au.dialog.Edit`

Adds Edit or ComboBox control.

```
public dialog Edit(DEdit editType, string editText = null, Strings comboItems = default)
```

##### Parameters

- *editType*  (`Au.Types.DEdit`):
    Control type/style.
- *editText*  (`string`):
    Initial edit field text.
- *comboItems*  (`Au.Types.Strings`):
    Combo box items used when *editType* is `Au.Types.DEdit.Combo`.

##### Returns

`Au.dialog`

#### Remarks

To get control text after closing the dialog, use `Au.dialog.Controls`.

Dialogs with an input field cannot have a progress bar.