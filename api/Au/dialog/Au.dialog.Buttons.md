# Method `Au.dialog.Buttons`

Sets buttons.

```
public dialog Buttons(Strings buttons = default, bool asCommandLinks = false)
```

##### Parameters

- *buttons*  (`Au.Types.Strings`):
    List of button names or `"id name"`. Examples: `"OK|Cancel"`, `"1 Yes|2 No"`, `"1 &Save|2 Do&n't Save|0 Cancel"`, `["1 One", "2 Two"]`. Can contain common buttons (named **OK**, **Yes**, **No**, **Retry**, **Cancel**, **Close**) and/or custom buttons (any other names). This first in the list button will be focused (aka *default button*). More info in Remarks.
- *asCommandLinks*  (`bool`):
    The style of custom buttons. If `false` - row of classic buttons. If `true` - column of command-link buttons that can have multiline text.

##### Returns

`Au.dialog`

#### Remarks

If buttons not set, the dialog will have **OK** button, id 1.

Missing ids are auto-generated, for example `"OK|Cancel|100 Custom1|Custom2"` is the same as `"1 OK|2 Cancel|100 Custom1|101 Custom2"`.

The first in the list button is the default button, ie is focused and therefore responds to the `Enter` key. For example, `"2 No|1 Yes"` adds **Yes** and **No** buttons and makes **No** default.

To create keyboard shortcuts, use `&` character in custom button labels. Use `&&` for literal `&`. Example: `"1 &Tuesday[]2 T&hursday[]3 Saturday && Sunday"`.

Trims newlines around ids and labels. For example, `"\r\n1 One\r\n|\r\n2\r\nTwo\r\n\r\n"` is the same as `"1 One|2 Two"`.

There are 6 *common buttons*: **OK**, **Yes**, **No**, **Retry**, **Cancel**, **Close**. Buttons that have other names are *custom buttons*. How common buttons are different:

1. The button style is not affected by *asCommandLinks* or `Au.Types.DFlags.CommandLinks`.
2. They have keyboard shortcuts that cannot be changed. Inserting `&` in a label makes it a custom button.
3. Button **Cancel** can be selected with the `Esc` key. It also adds **X** (Close) button in title bar, which selects **Cancel**.
4. Always displayed in standard order (eg **Yes** **No**, never **No** **Yes**). But you can for example use `"2 No|1 Yes"` to set default button = **No**.
5. The displayed button label is localized, ie different when the Windows UI language is not English.