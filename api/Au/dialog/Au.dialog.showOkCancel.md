# Method `Au.dialog.showOkCancel`

Shows dialog with **OK** and **Cancel** buttons.

```
public static bool showOkCancel(string text1 = null, DText text2 = null, DFlags flags = 0, DIcon icon = 0, AnyWnd owner = default, DText expandedText = null, string title = null, int secondsTimeout = 0)
```

##### Parameters

- *text1*  (`string`):
    Heading text.
- *text2*  (`Au.Types.DText`):
    Message text. Can be string, or string with links like `new("Text <a>link</a> text.", e => { print.it("link"); })`.
- *flags*  (`Au.Types.DFlags`)
- *icon*  (`Au.Types.DIcon`)
- *owner*  (`Au.Types.AnyWnd`):
    Owner window. See `Au.dialog.OwnerWindow`.
- *expandedText*  (`Au.Types.DText`):
    Text in expander control. Can be string, or string with links like `new("Text <a>link</a> text.", e => { print.it("link"); })`.
- *title*  (`string`):
    Title bar text. If omitted, `null` or `""`, uses `Au.dialog.options.defaultTitle`.
- *secondsTimeout*  (`int`):
    If not 0, after this time (seconds) auto-close the dialog and return `Au.dialog.Timeout`.

##### Returns

`bool`

`true` if selected **OK**.

##### Exceptions

- `Win32Exception`:
    Failed to show dialog. Unlikely.

#### Remarks

Calls `Au.dialog.show`.