# Method `Au.dialog.showInput`

Shows dialog with a text edit field and gets that text.

```
public static bool showInput(out string s, string text1 = null, DText text2 = null, DEdit editType = DEdit.Text, string editText = null, Strings comboItems = default, DFlags flags = 0, AnyWnd owner = default, DText expandedText = null, DText footer = null, string title = null, DControls controls = null, Coord x = default, Coord y = default, screen screen = default, int secondsTimeout = 0, string buttons = "1 OK|2 Cancel", Action<DEventArgs> onButtonClick = null)
```

##### Parameters

- *s*  (`string`):
    Variable that receives the text.
- *text1*  (`string`):
    Heading text.
- *text2*  (`Au.Types.DText`):
    Message test (above the edit field).
- *editType*  (`Au.Types.DEdit`):
    Edit field type. It can be simple text (default), multiline, number, password or combo box.
- *editText*  (`string`):
    Initial edit field text.
- *comboItems*  (`Au.Types.Strings`):
    Combo box items used when *editType* is `Au.Types.DEdit.Combo`.
- *flags*  (`Au.Types.DFlags`)
- *owner*  (`Au.Types.AnyWnd`):
    Owner window. See `Au.dialog.OwnerWindow`.
- *expandedText*  (`Au.Types.DText`):
    Text in expander control.
- *footer*  (`Au.Types.DText`):
    Text at the bottom of the dialog. Icon can be specified like `"i|Text"`, where `i` is: `x` error, `!` warning, `i` info, `v` shield, `a` app.
- *title*  (`string`):
    Title bar text. If omitted, `null` or `""`, uses `Au.dialog.options.defaultTitle`.
- *controls*  (`Au.Types.DControls`):
    Can be used to add more controls and later get their values: checkbox, radio buttons.
- *x*  (`Au.Types.Coord`):
    X position in screen. Default - screen center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y position in screen. Default - screen center.
- *screen*  (`Au.screen`):
    See `Au.dialog.InScreen`. Examples: `screen.ofMouse`, `screen.index(1)`.
- *secondsTimeout*  (`int`):
    If not 0, after this time (seconds) auto-close the dialog and return `Au.dialog.Timeout`.
- *buttons*  (`string`):
    Buttons. List of names or `"id name"`. Example: `"1 OK|2 Cancel|10 Browse..."`. See `Au.dialog.Buttons`. Note: this function returns `true` only when clicked button with id 1. Usually custom buttons are used with *onButtonClick* function, which for example can get button id or disable closing the dialog.
- *onButtonClick*  (`Action<Au.Types.DEventArgs>`):
    A button-clicked event handler function. See examples.

##### Returns

`bool`

`true` if selected **OK** (or a custom button with id 1).

##### Exceptions

- `Win32Exception`:
    Failed to show dialog.

#### Remarks

This function allows you to use many dialog features, but not all. Alternatively you can create a `Au.dialog` class instance, call `Au.dialog.Edit` or use the *controls* parameter, set other properties and call `Au.dialog.ShowDialog`.

#### Examples

Simple.

```
string s;
if(!dialog.showInput(out s, "Example")) return;
print.it(s);

if(!dialog.showInput(out var s2, "Example")) return;
print.it(s2);
```

With checkbox.

```
var con = new DControls { Checkbox = "Check" };
if(!dialog.showInput(out var s, "Example", "Comments.", controls: con)) return;
print.it(s, con.IsChecked);
```

With *onButtonClick* function.

```
int r = 0;
dialog.showInput(out string s, "Example", buttons: "OK|Cancel|Later", onButtonClick: e => r = e.Button);
print.it(r);

if(!dialog.showInput(out string s, "Example", flags: DFlags.CommandLinks, buttons: "OK|Cancel|10 Set text", onButtonClick: e => {
	if(e.Button == 10) { e.EditText = "text"; e.DontCloseDialog = true; }
})) return;

if(!dialog.showInput(out string s2, "Example", "Try to click OK while text is empty.", onButtonClick: e => {
	if(e.Button == 1 && e.EditText.NE()) {
		dialog.show("Text cannot be empty.", owner: e.hwnd);
		e.d.EditControl.Focus();
		e.DontCloseDialog = true;
	}
})) return;
```