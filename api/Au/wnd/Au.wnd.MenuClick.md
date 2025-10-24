# Method `Au.wnd.MenuClick`

Posts a "menu item clicked" notification (`WM_COMMAND`) as if that menu item has been clicked. Does not use the mouse.

```
public void MenuClick(int itemId, bool systemMenu = false)
```

##### Parameters

- *itemId*  (`int`):
    Menu item id. Must be in range 1 to 0xffff.
- *systemMenu*  (`bool`):
    The menu item is in the title bar's context menu, not in the menu bar. Posts `WM_SYSCOMMAND` instead.

##### Exceptions

- `Au.Types.AuWndException`:
    Invalid window.
- `ArgumentOutOfRangeException`:
    Invalid *itemId*.

#### Remarks

Works only with classic menus. The drop-down menu window class name must be `"#32768"`. Works with menu items in window menu bar, system menu and some context menus. Does not use the menu itself. Just posts `WM_COMMAND` or `WM_SYSCOMMAND` message. Even if a menu item with this id does not exist. This variable is the window that contains the menu bar or system menu. Or the drop-down menu window (class `"#32768"`) that contains the menu item.