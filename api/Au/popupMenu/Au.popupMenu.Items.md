# Property `Au.popupMenu.Items`

Gets added items, except separators and items in submenus.

```
public IEnumerable<PMItem> Items { get; }
```

##### Property Value

`IEnumerable<Au.Types.PMItem>`

#### Remarks

Allows to set properties of multiple items in single place instead of after each "add item" code line.

Does not get items in submenus. Submenus are separate `Au.popupMenu` objects and you can use their `Items` property.