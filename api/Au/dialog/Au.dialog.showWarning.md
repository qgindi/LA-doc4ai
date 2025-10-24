# Method `Au.dialog.showWarning`

Shows dialog with `Au.Types.DIcon.Warning` icon.

```
public static int showWarning(string text1 = null, DText text2 = null, Strings buttons = default, DFlags flags = 0, AnyWnd owner = default, DText expandedText = null, string title = null, int secondsTimeout = 0)
```

##### Parameters

- *text1*  (`string`):
    Heading text.
- *text2*  (`Au.Types.DText`):
    Message text. Can be string, or string with links like `new("Text <a>link</a> text.", e => { print.it("link"); })`.
- *buttons*  (`Au.Types.Strings`):
    List of button names or `"id name"`. Examples: `"OK|Cancel"`, `"1 Yes|2 No"`, `"1 &Save|2 Do&n't Save|0 Cancel"`, `["1 One", "2 Two"]`. Can contain common buttons (named **OK**, **Yes**, **No**, **Retry**, **Cancel**, **Close**) and/or custom buttons (any other names). This first in the list button will be focused (aka *default button*). More info: `Au.dialog.Buttons`.
- *flags*  (`Au.Types.DFlags`)
- *owner*  (`Au.Types.AnyWnd`):
    Owner window. See `Au.dialog.OwnerWindow`.
- *expandedText*  (`Au.Types.DText`):
    Text in expander control. Can be string, or string with links like `new("Text <a>link</a> text.", e => { print.it("link"); })`.
- *title*  (`string`):
    Title bar text. If omitted, `null` or `""`, uses `Au.dialog.options.defaultTitle`.
- *secondsTimeout*  (`int`):
    If not 0, after this time (seconds) auto-close the dialog and return `Au.dialog.Timeout`.

##### Returns

`int`

Selected button id.

##### Exceptions

- `Win32Exception`:
    Failed to show dialog. Unlikely.

#### Remarks

Calls `Au.dialog.show`.