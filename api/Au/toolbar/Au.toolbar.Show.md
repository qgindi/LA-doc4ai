# Method `Au.toolbar.Show`

## Overload 1

Shows the toolbar.

```
public void Show(screen screen = default)
```

##### Parameters

- *screen*  (`Au.screen`):
    Attach to this screen. For example a screen index (0 the primary, 1 the first non-primary, and so on). Example: `screen.index(1)`. If not specified, the toolbar will be attached to the screen where it is now or where will be moved later. Don't use this parameter if this toolbar was created by `Au.toolbar.AutoHideScreenEdge`, because then screen is already known.

##### Exceptions

- `ArgumentException`:
    The toolbar was created by `Au.toolbar.AutoHideScreenEdge`, and now screen specified again.
- `InvalidOperationException`:
    `Show` already called.

#### Remarks

The toolbar will be moved when the screen moved or resized.

* * *

## Overload 2

Shows the toolbar and attaches to a window.

```
public void Show(wnd ownerWindow, bool clientArea = false)
```

##### Parameters

- *ownerWindow*  (`Au.wnd`):
    Window or control. Can belong to any process.
- *clientArea*  (`bool`):
    Let the toolbar position be relative to the client area of the window.

##### Exceptions

- `InvalidOperationException`:
    `Show` already called.
- `ArgumentException`:
    *ownerWindow* is 0.

#### Remarks

The toolbar will be above the window in the Z order; moved when the window moved or resized; hidden when the window hidden, cloaked or minimized; destroyed when the window destroyed.

* * *

## Overload 3

Shows the toolbar and attaches to an object in a window.

```
public void Show(wnd ownerWindow, ITBOwnerObject oo)
```

##### Parameters

- *ownerWindow*  (`Au.wnd`):
    Window that contains the object. Can be control. Can belong to any process.
- *oo*  (`Au.Types.ITBOwnerObject`):
    A variable of a user-defined class that implements `Au.Types.ITBOwnerObject` interface. It provides object location, visibility, etc.

##### Exceptions

- `InvalidOperationException`:
    `Show` already called.
- `ArgumentException`:
    *ownerWindow* is 0.

#### Remarks

The toolbar will be above the window in the Z order; moved when the object or window moved or resized; hidden when the object or window hidden, cloaked or minimized; destroyed when the object or window destroyed.

* * *

## Overload 4

Shows the toolbar. If *ta* is `Au.Triggers.WindowTriggerArgs`, attaches the toolbar to the trigger window. Else if *ta* != `null`, calls `Au.Triggers.TriggerArgs.DisableTriggerUntilClosed`.

```
public void Show(TriggerArgs ta)
```

##### Parameters

- *ta*  (`Au.Triggers.TriggerArgs`)