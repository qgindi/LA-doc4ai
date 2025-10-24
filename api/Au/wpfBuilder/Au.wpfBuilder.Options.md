# Method `Au.wpfBuilder.Options`

Changes some options for elements added afterwards.

```
public wpfBuilder Options(bool? modifyPadding = null, bool? rightAlignLabels = null, Thickness? margin = null, bool? showToolTipOnKeyboardFocus = null, bool? bindLabelVisibility = null)
```

##### Parameters

- *modifyPadding*  (`bool?`):
    Let `Add` adjust the `Padding` property of some controls to align content better when using default theme. Default value of this option depends on application's theme.
- *rightAlignLabels*  (`bool?`):
    Right-align `System.Windows.Controls.Label` controls in grid cells.
- *margin*  (`Thickness?`):
    Default margin of elements. If not set, default margin is 3 in all sides. Default margin of nested panels is 0; this option is not used.
- *showToolTipOnKeyboardFocus*  (`bool?`):
    Show tooltips when the tooltip owner element receives the keyboard focus when using keys to focus controls or open the window. If `true`, it can be set separately for each tooltip or owner element with `System.Windows.Controls.ToolTip.ShowsToolTipOnKeyboardFocus` or `System.Windows.Controls.ToolTipService.SetShowsToolTipOnKeyboardFocus`.
- *bindLabelVisibility*  (`bool?`):
    Let `Au.wpfBuilder.LabeledBy` and an `Add` overload that adds 2 elements (the first is `System.Windows.Controls.Label`) bind the `Visibility` property of the label to that of the last added element, to automatically hide/show the label together with the element. Also binds `IsEnabled` if it is `System.Windows.Controls.Label` or `System.Windows.Controls.TextBlock`.

##### Returns

`Au.wpfBuilder`