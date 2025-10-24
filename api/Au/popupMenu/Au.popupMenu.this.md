# Indexer of `Au.popupMenu`

Adds menu item with action (callback function) that is executed on click.

```
public Action<PMItem> this[string text, MTImage image = default, bool disable = false, int l_ = 0, string f_ = null] { set; }
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

##### Property Value

`Action<Au.Types.PMItem>`

Action executed on click. Can be `null`.

#### Remarks

This function is the same as `Au.popupMenu.Add`. The difference is, `Add` returns `Au.Types.PMItem` object of the added item. When using the indexer, to access the item use `Au.popupMenu.Last`. These codes are the same: `var v=m.Add("text", o=>{});"` and `m["text"]=o=>{}; var v=m.Last;`.