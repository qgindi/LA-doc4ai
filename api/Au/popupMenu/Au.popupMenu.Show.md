# Method `Au.popupMenu.Show`

Shows the menu and waits until closed.

```
public int Show(PMFlags flags = 0, POINT? xy = null, RECT? excludeRect = null, AnyWnd owner = default)
```

##### Parameters

- *flags*  (`Au.Types.PMFlags`)
- *xy*  (`Au.Types.POINT?`):
    Menu position in screen. If `null` (default), uses mouse position by default. It depends on *flags*.
- *excludeRect*  (`Au.Types.RECT?`):
    The menu should not overlap this rectangle in screen.
- *owner*  (`Au.Types.AnyWnd`):
    Owner window. The menu will be automatically closed when destroying its owner window.

##### Returns

`int`

id of the selected item, or 0 if canceled. See also: `Au.popupMenu.Result`.

##### Exceptions

- `InvalidOperationException`:
    The menu is open or is submenu.