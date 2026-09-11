# Method `Au.popupMenu.AddCheck`

Adds menu item to be used as a checkbox.

```csharp
public PMItem AddCheck(string text, bool check = false, Action<PMItem> click = null, bool disable = false, MTImage image = default, int l_ = 0, string f_ = null)
```

##### Parameters

- *text*  (`string`):
  Item text. Can include hotkey, tooltip and underlined character, like `"Te&xt\t Hotkey\0 Tooltip"`; more info: `Au.popupMenu`.
- *check*  (`bool`):
  Checked state.
- *click*  (`Action<Au.Types.PMItem>`):
  Action executed on click.
- *disable*  (`bool`):
  Disabled state.
- *image*  (`Au.Types.MTImage`):
  Item image. Read here: `Au.Types.MTBase`.
- *l_*  (`int`):
  [Caller info parameter](🔗)
- *f_*  (`string`):
  [Caller info parameter](🔗)

##### Returns

`Au.Types.PMItem`

#### Remarks

When clicked, `Au.Types.PMItem.IsChecked` state is changed.