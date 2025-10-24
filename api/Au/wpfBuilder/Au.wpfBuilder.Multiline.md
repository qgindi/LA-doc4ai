# Method `Au.wpfBuilder.Multiline`

Makes the last added `System.Windows.Controls.TextBox` multiline.

```
public wpfBuilder Multiline(WBLength? height = null, TextWrapping wrap = TextWrapping.WrapWithOverflow)
```

##### Parameters

- *height*  (`Au.Types.WBLength?`):
    If not `null`, sets height or/and min/max height.
- *wrap*  (`TextWrapping`):
    Sets `System.Windows.Controls.TextBox.TextWrapping`.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `NotSupportedException`:
    The last added element is not `System.Windows.Controls.TextBox`.