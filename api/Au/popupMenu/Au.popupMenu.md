# Class `Au.popupMenu`

Popup menu.

```
public class popupMenu : MTBase
```

##### Remarks

Can be used everywhere: in automation scripts, WPF apps, other apps, etc. Also can be used as a popup list and supports many items with scrollbar.

Menu item text can include hotkey after `'\t'` character and/or tooltip after `'|'` or `'\0'` character. Examples: `"Text\t Hotkey"`, `"Text|Tooltip"`, `"Text\t Hotkey\0 Tooltip"`. Character with prefix `&` (eg `'A'` in `"Save &As"`) will be underlined (depends on Windows settings and `Au.Types.PMFlags`) and can be used to select the item with keyboard.

Keyboard, mouse:

- `Enter`, `Tab`, `Space` - close the menu and execute the focused item. Or show the submenu.
- `Esc` - close the menu or current submenu.
- `Left` - close current submenu.
- `Right` - open submenu.
- `Down`, `Up`, `PageDown`, `PageUp`, `End`, `Home` - focus other item.
- underlined menu item character - close the menu and execute the item. Or show the submenu. See `Au.Types.PMFlags.Underline`.
- `Alt`, `Win`, `F10`, `Apps`, `Back` - close menus.
- click outside - close the menu.
- middle click - close the menu.
- right click - show context menu (if used constructor with parameters).

While a menu is open, it captures many keyboard keys, even when its thread isn't the foreground thread.

Not thread-safe. All functions must be called in same thread, unless documented otherwise.

##### Examples

```
var m = new popupMenu("example");
m["One"] = o => print.it(o);
m["Two\0Tooltip", image: icon.stock(StockIcon.DELETE)] = o => { print.it(o); dialog.show(o.ToString()); };
m.Submenu("Submenu", m => {
	m["Three"] = o => print.it(o);
	m["Four"] = o => print.it(o);
});
m["notepad"] = o => run.itSafe(folders.System + "notepad.exe");
m.Show();
```

##### Inheritance

`object` → `Au.Types.MTBase` → `popupMenu`

### Constructors

`popupMenu()`, `popupMenu(string, string, int)`

### Properties

`CheckDontClose`, `FocusedItem`, `Font`, `IsOpen`, `this[string, MTImage, bool, int, string]`, `Items`, `ItemsAndSeparators`, `KeyboardHook`, `Last`, `Metrics`, `RawText`, `Result`, `caretRectFunc`, `defaultFont`, `defaultMetrics`

### Methods

`Add`, `Add`, `Add`, `AddCheck`, `AddRadio`, `Close`, `Separator`, `Show`, `Submenu`, `Submenu`, `showSimple`

### Members inherited from other types of this library
`MTBase.ExtractIconPathFromCode`, `MTBase.ActionThread`, `MTBase.ActionException`, `MTBase.PathInTooltip`, `MTBase.ImageSize`