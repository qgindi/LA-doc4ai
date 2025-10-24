# Property `Au.popupMenu.FocusedItem`

Gets or sets the focused menu item.

```
public PMItem FocusedItem { get; set; }
```

##### Property Value

`Au.Types.PMItem`

#### Remarks

The focused item visually shows the menu item that would be executed if clicked or pressed `Enter`, `Tab` or `Space` key. It changes when the user moves the mouse or presses navigation keys (arrows, `End`, `Home`, `PageDown`, `PageUp`). This property can be set before showing the menu or when it is open.