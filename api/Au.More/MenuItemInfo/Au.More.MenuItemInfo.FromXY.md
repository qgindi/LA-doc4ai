# Method `Au.More.MenuItemInfo.FromXY`

## Overload 1

Gets info of a menu item from point.

```
public static MenuItemInfo FromXY(POINT pScreen, wnd w, int msTimeout = 5000)
```

##### Parameters

- *pScreen*  (`Au.Types.POINT`):
    Point in screen coordinates.
- *w*  (`Au.wnd`):
    Popup menu window, class name `"#32768"`.
- *msTimeout*  (`int`):
    Timeout (ms) to use when the window is busy or hung.

##### Returns

`Au.More.MenuItemInfo`

`null` if failed, eg the point is not in the menu or the window is hung.

* * *

## Overload 2

Gets info of a menu item from mouse.

```
public static MenuItemInfo FromXY(int msTimeout = 5000)
```

##### Parameters

- *msTimeout*  (`int`):
    Timeout (ms) to use when the window is busy or hung.

##### Returns

`Au.More.MenuItemInfo`

`null` if failed, eg the point is not in a menu or the window is hung.