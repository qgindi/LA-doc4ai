# Method `Au.Triggers.AutotextTriggerArgs.Menu`

Creates and shows a menu below the text cursor (caret) or mouse cursor, and calls `Au.Triggers.AutotextTriggerArgs.Replace`.

```
public void Menu(params TAMenuItem[] items)
```

##### Parameters

- *items*  (`Au.Triggers.TAMenuItem[]`):

    Menu items. An item can be specified as:

    - string - the replacement text. Also it's the menu item label.
    - `Au.Triggers.TAMenuItem` - allows to set custom label and the replacement text and/or HTML.
    - `null` - separator. 
Label can contain tooltip like `"Text\0 Tooltip"`. Replacement text can contain `[[|]]` to move the caret there (see `Au.Triggers.AutotextTriggerArgs.Replace`).

#### Remarks

Keyboard:

- `Esc` - close the menu.
- `Enter`, `Tab` - select the focused or the first item.
- `Down`, `Up`, `End`, `Home`, `PageDown`, `PageUp` - focus menu items.
- Also to select menu items can type the number characters displayed at the right.
- Other keys close the menu and are passed to the active window.

#### Examples

Code in file `Autotext triggers`.

```
//var tt = Triggers.Autotext;
tt["m1"] = o => o.Menu([
	"https://www.example.com",
	"<tag>[[|]]</tag>",
	new("Label example", "TEXT1"),
	null,
	new("HTML example", "TEXT2", "<b>TEXT2</b>"),
	new(null, "TEXT3"),
	]);
```

### See Also

`Au.Triggers.AutotextTriggers.MenuOptions`

`Au.popupMenu.defaultFont`

`Au.popupMenu.defaultMetrics`