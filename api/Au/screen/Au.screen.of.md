# Method `Au.screen.of`

## Overload 1

Gets screen containing the biggest part of the specified window or nearest to it.

```
public static screen of(wnd w, SODefault defaultScreen = SODefault.Nearest, bool lazy = false)
```

##### Parameters

- *w*  (`Au.wnd`):
    Window or control. If `default(wnd)` or invalid, gets the primary screen.
- *defaultScreen*  (`Au.Types.SODefault`)
- *lazy*  (`bool`):

    Create variable with `Au.screen.LazyFunc` that later will get screen handle. Other ways to create lazy:

    - use `Au.wndFinder`. Example: `screen.of(new wndFinder("* Notepad"))`.
    - use constructor. Example: `new screen(() => screen.of(wnd.findFast(cn: "Notepad")))`.

##### Returns

`Au.screen`

* * *

## Overload 2

Gets screen containing the biggest part of the specified window or nearest to it.

```
public static screen of(wndFinder f, SODefault defaultScreen = SODefault.Nearest, bool lazy = true)
```

##### Parameters

- *f*  (`Au.wndFinder`):
    Window finder. If window not found, gets the primary screen.
- *defaultScreen*  (`Au.Types.SODefault`)
- *lazy*  (`bool`):
    Create variable with `Au.screen.LazyFunc` that later will find window and get screen handle. Default `true`.

##### Returns

`Au.screen`

* * *

## Overload 3

Gets screen containing the biggest part of the specified winforms window or control or nearest to it.

```
public static screen of(Control c, SODefault defaultScreen = SODefault.Nearest, bool lazy = false)
```

##### Parameters

- *c*  (`Control`):
    Window or control. If handle not created, gets the primary screen. Cannot be `null`.
- *defaultScreen*  (`Au.Types.SODefault`)
- *lazy*  (`bool`):
    Create variable with `Au.screen.LazyFunc` that later will get screen handle.

##### Returns

`Au.screen`

* * *

## Overload 4

Gets screen containing the biggest part of the specified WPF window or nearest to it.

```
public static screen of(Window w, SODefault defaultScreen = SODefault.Nearest, bool lazy = false)
```

##### Parameters

- *w*  (`Window`):
    WPF window. If handle not created, gets the primary screen. Cannot be `null`.
- *defaultScreen*  (`Au.Types.SODefault`)
- *lazy*  (`bool`):
    Create variable with `Au.screen.LazyFunc` that later will get screen handle.

##### Returns

`Au.screen`

* * *

## Overload 5

Gets screen containing the biggest part of the specified WPF element (of its rectangle) or nearest to it.

```
public static screen of(FrameworkElement elem, SODefault defaultScreen = SODefault.Nearest, bool lazy = false)
```

##### Parameters

- *elem*  (`FrameworkElement`):
    WPF element. If not loaded, gets the primary screen. Cannot be `null`.
- *defaultScreen*  (`Au.Types.SODefault`)
- *lazy*  (`bool`):
    Create variable with `Au.screen.LazyFunc` that later will get screen handle.

##### Returns

`Au.screen`

* * *

## Overload 6

Gets screen containing the specified point or nearest to it.

```
public static screen of(POINT p, SODefault defaultScreen = SODefault.Nearest, bool lazy = false)
```

##### Parameters

- *p*  (`Au.Types.POINT`)
- *defaultScreen*  (`Au.Types.SODefault`)
- *lazy*  (`bool`):
    Create variable with `Au.screen.LazyFunc` that later will get screen handle.

##### Returns

`Au.screen`

* * *

## Overload 7

Gets screen containing the specified point or nearest to it.

```
public static screen of(int x, int y, SODefault defaultScreen = SODefault.Nearest, bool lazy = false)
```

##### Parameters

- *x*  (`int`)
- *y*  (`int`)
- *defaultScreen*  (`Au.Types.SODefault`)
- *lazy*  (`bool`):
    Create variable with `Au.screen.LazyFunc` that later will get screen handle.

##### Returns

`Au.screen`

* * *

## Overload 8

Gets screen containing the biggest part of the specified rectangle or nearest to it.

```
public static screen of(RECT r, SODefault defaultScreen = SODefault.Nearest, bool lazy = false)
```

##### Parameters

- *r*  (`Au.Types.RECT`)
- *defaultScreen*  (`Au.Types.SODefault`)
- *lazy*  (`bool`):
    Create variable with `Au.screen.LazyFunc` that later will get screen handle.

##### Returns

`Au.screen`