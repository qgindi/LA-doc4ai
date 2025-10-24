# Method `Au.dialog.showList`

Shows dialog with a list of command-link buttons, and returns 1-based button index or 0.

```
public static int showList(Strings list, string text1 = null, DText text2 = null, DFlags flags = 0, AnyWnd owner = default, DText expandedText = null, DText footer = null, string title = null, DControls controls = null, Coord x = default, Coord y = default, screen screen = default, int secondsTimeout = 0)
```

##### Parameters

- *list*  (`Au.Types.Strings`):
    List items (buttons). Can be like `"One|Two|Three"` or `new("One", "Two", "Three")` or string array or `List`. See `Au.dialog.Buttons`.
- *text1*  (`string`):
    Heading text.
- *text2*  (`Au.Types.DText`):
    Message text.
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
    Can be used to add more controls and later get their values: checkbox, radio buttons, text input.
- *x*  (`Au.Types.Coord`):
    X position in screen. Default - screen center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y position in screen. Default - screen center.
- *screen*  (`Au.screen`):
    See `Au.dialog.InScreen`. Examples: `screen.ofMouse`, `screen.index(1)`.
- *secondsTimeout*  (`int`):
    If not 0, after this time (seconds) auto-close the dialog and return `Au.dialog.Timeout`.

##### Returns

`int`

1-based index of the selected button. Returns 0 if clicked the **X** (close window) button or pressed `Esc`.

##### Exceptions

- `Win32Exception`:
    Failed to show dialog.

#### Remarks

This function allows you to use most of the dialog features, but not all. Alternatively you can create a `Au.dialog` class instance, set properties and call `Au.dialog.ShowDialog`. Example in `Au.dialog` class help.

#### Examples

```
int r = dialog.showList("One|Two|Three", "Example", y: -1, secondsTimeout: 15);
if(r <= 0) return; //X/Esc or timeout
print.it(r);
```

### See Also

`Au.popupMenu.showSimple`