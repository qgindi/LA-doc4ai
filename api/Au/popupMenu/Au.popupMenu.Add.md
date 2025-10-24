# Method `Au.popupMenu.Add`

## Overload 1

Adds menu item with explicitly specified id.

```
public PMItem Add(int id, string text, MTImage image = default, bool disable = false, int l_ = 0, string f_ = null)
```

##### Parameters

- *id*  (`int`):
    Item id that `Au.popupMenu.Show` will return if clicked this item.
- *text*  (`string`):
    Item text. Can include hotkey, tooltip and underlined character, like `"Te&xt\t Hotkey\0 Tooltip"`; more info: `Au.popupMenu`.
- *image*  (`Au.Types.MTImage`):
    Item image. Read here: `Au.Types.MTBase`.
- *disable*  (`bool`):
    Disabled state.
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

##### Returns

`Au.Types.PMItem`

* * *

## Overload 2

Adds menu item with auto-generated id.

```
public PMItem Add(string text, MTImage image = default, bool disable = false, int l_ = 0, string f_ = null)
```

##### Parameters

- *text*  (`string`):
    Item text. Can include hotkey, tooltip and underlined character, like `"Te&xt\t Hotkey\0 Tooltip"`; more info: `Au.popupMenu`.
- *image*  (`Au.Types.MTImage`):
    Item image. Read here: `Au.Types.MTBase`.
- *disable*  (`bool`):
    Disabled state.
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

##### Returns

`Au.Types.PMItem`

#### Remarks

Assigns id = the last specified or auto-generated id + 1. If not using explicitly specified ids, auto-generated ids are 1, 2, 3... Submenu-items, separators and items with action don't auto-generate ids.

* * *

## Overload 3

Adds menu item with action (callback function) that is executed on click.

```
public PMItem Add(string text, Action<PMItem> click, MTImage image = default, bool disable = false, int l_ = 0, string f_ = null)
```

##### Parameters

- *text*  (`string`):
    Item text. Can include hotkey, tooltip and underlined character, like `"Te&xt\t Hotkey\0 Tooltip"`; more info: `Au.popupMenu`.
- *click*  (`Action<Au.Types.PMItem>`):
    Action executed on click.
- *image*  (`Au.Types.MTImage`):
    Item image. Read here: `Au.Types.MTBase`.
- *disable*  (`bool`):
    Disabled state.
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

##### Returns

`Au.Types.PMItem`

#### Remarks

This function is the same as the indexer. The difference is, `Add` returns `Au.Types.PMItem` object of the added item. When using the indexer, to access the item use `Au.popupMenu.Last`. These codes are the same: `var v=m.Add("text", o=>{});"` and `m["text"]=o=>{}; var v=m.Last;`.