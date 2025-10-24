# Method `Au.dialog.showProgress`

Shows dialog with progress bar. Creates dialog in new thread and returns without waiting until it is closed.

```
public static dialog showProgress(bool marquee, string text1 = null, DText text2 = null, string buttons = "0 Cancel", DFlags flags = 0, AnyWnd owner = default, DText expandedText = null, DText footer = null, string title = null, DControls controls = null, Coord x = default, Coord y = default, screen screen = default, int secondsTimeout = 0)
```

##### Parameters

- *marquee*  (`bool`):
    Let the progress bar animate without indicating a percent of work done.
- *text1*  (`string`):
    Heading text.
- *text2*  (`Au.Types.DText`):
    Message text. Can be string, or string with links like `new("Text <a>link</a> text.", e => { print.it("link"); })`.
- *buttons*  (`string`):
    List of button names or `"id name"`. Examples: `"OK|Cancel"`, `"1 Yes|2 No"`, `"1 &Save|2 Do&n't Save|0 Cancel"`, `["1 One", "2 Two"]`. Can contain common buttons (named **OK**, **Yes**, **No**, **Retry**, **Cancel**, **Close**) and/or custom buttons (any other names). This first in the list button will be focused (aka *default button*). More info: `Au.dialog.Buttons`.
- *flags*  (`Au.Types.DFlags`)
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

##### Returns

`Au.dialog`

Variable that can be used to communicate with the dialog using these methods and properties: `Au.dialog.IsOpen`, `Au.dialog.ThreadWaitForClosed`, `Au.dialog.Result` (when closed), `Au.dialog.Controls` (when closed), `Au.dialog.DialogWindow`, `Au.dialog.Send`; through the `Send` property you can set progress, modify controls and close the dialog (see example).

##### Exceptions

- `Win32Exception`:
    Failed to show dialog. Unlikely.

#### Remarks

This function allows you to use most of the dialog features, but not all. Alternatively you can create a `Au.dialog` class instance, set properties and call `Au.dialog.ShowDialogNoWait`.

#### Examples

```
var pd = dialog.showProgress(false, "Working", buttons: "1 Stop", y: -1);
for(int i = 1; i <= 100; i++) {
	if(!pd.IsOpen) { print.it(pd.Result); break; } //if the user closed the dialog
	pd.Send.Progress(i); //don't need this if marquee
	50.ms(); //do something in the loop
}
pd.Send.Close();
```