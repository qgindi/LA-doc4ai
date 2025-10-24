# Constructor of `Au.dialog`

Initializes a new `Au.dialog` instance and sets main properties.

```
public dialog(string text1 = null, DText text2 = null, Strings buttons = default, DFlags flags = 0, DIcon icon = 0, AnyWnd owner = default, DText expandedText = null, DText footer = null, string title = null, DControls controls = null, Coord x = default, Coord y = default, screen screen = default, int secondsTimeout = 0)
```

##### Parameters

- *text1*  (`string`):
    Heading text.
- *text2*  (`Au.Types.DText`):
    Message text. Can be string, or string with links like `new("Text <a>link</a> text.", e => { print.it("link"); })`.
- *buttons*  (`Au.Types.Strings`):
    List of button names or `"id name"`. Examples: `"OK|Cancel"`, `"1 Yes|2 No"`, `"1 &Save|2 Do&n't Save|0 Cancel"`, `["1 One", "2 Two"]`. Can contain common buttons (named **OK**, **Yes**, **No**, **Retry**, **Cancel**, **Close**) and/or custom buttons (any other names). This first in the list button will be focused (aka *default button*). More info: `Au.dialog.Buttons`.
- *flags*  (`Au.Types.DFlags`)
- *icon*  (`Au.Types.DIcon`)
- *owner*  (`Au.Types.AnyWnd`):
    Owner window. See `Au.dialog.OwnerWindow`.
- *expandedText*  (`Au.Types.DText`):
    Text in expander control. Can be string, or string with links like `new("Text <a>link</a> text.", e => { print.it("link"); })`.
- *footer*  (`Au.Types.DText`):
    Text at the bottom of the dialog. Can be string, or string with links like `new("Text <a>link</a> text.", e => { print.it("link"); })`. Icon can be specified like `"i|Text"`, where `i` is: `x` error, `!` warning, `i` info, `v` shield, `a` app.
- *title*  (`string`):
    Title bar text. If omitted, `null` or `""`, uses `Au.dialog.options.defaultTitle`.
- *controls*  (`Au.Types.DControls`):
    Can be used to add more controls and later get their values: checkbox, radio buttons, text input.
- *x*  (`Au.Types.Coord`):
    X position in screen. Default - screen center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y position in screen. Default - screen center.
- *screen*  (`Au.screen`):
    See `Au.dialog.InScreen`. Examples: `screen.ofMouse`, `screen.at.left()`.
- *secondsTimeout*  (`int`):
    If not 0, after this time (seconds) auto-close the dialog and return `Au.dialog.Timeout`.