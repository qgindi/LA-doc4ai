# Method `Au.dialog.showInputNumber`

Shows dialog with a number edit field and gets that number.

```
public static bool showInputNumber(out int i, string text1 = null, DText text2 = null, int? editText = null, DFlags flags = 0, AnyWnd owner = default)
```

##### Parameters

- *i*  (`int`):
    Variable that receives the number.
- *text1*  (`string`):
    Heading text.
- *text2*  (`Au.Types.DText`):
    Message text (above the edit field).
- *editText*  (`int?`):
    Initial edit field text.
- *flags*  (`Au.Types.DFlags`)
- *owner*  (`Au.Types.AnyWnd`):
    Owner window. See `Au.dialog.OwnerWindow`.

##### Returns

`bool`

`true` if selected **OK**.

##### Exceptions

- `Win32Exception`:
    Failed to show dialog.

#### Remarks

Calls `Au.dialog.showInput` and converts string to `int`.

#### Examples

```
int i;
if(!dialog.showInputNumber(out i, "Example")) return;
print.it(i);
```