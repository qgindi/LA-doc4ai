# Method `Au.wpfBuilder.Readonly`

Sets `System.Windows.Controls.Primitives.TextBoxBase.IsReadOnly` or `System.Windows.Controls.ComboBox.IsReadOnly` of the last added text box or editable combo box.

```
public wpfBuilder Readonly(bool readOnly = true, bool caretVisible = false)
```

##### Parameters

- *readOnly*  (`bool`)
- *caretVisible*  (`bool`):
    Sets `System.Windows.Controls.Primitives.TextBoxBase.IsReadOnlyCaretVisible`. Not used with `System.Windows.Controls.ComboBox`.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    The last added element is not `System.Windows.Controls.Primitives.TextBoxBase` or `System.Windows.Controls.ComboBox`.