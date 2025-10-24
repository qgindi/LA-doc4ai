# Method `Au.popupMenu.Close`

Closes the menu and its submenus.

```
public void Close(bool ancestorsToo = false)
```

##### Parameters

- *ancestorsToo*  (`bool`):
    If this is a submenu, close the root menu with all submenus.

#### Remarks

Can be called from any thread. Does nothing if not open.