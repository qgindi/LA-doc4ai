# Method `Au.wnd.getwnd.SiblingBelow`

## Overload 1

Gets nearest visible sibling control to below this.

```
public wnd SiblingBelow()
```

##### Returns

`Au.wnd`

`default(wnd)` if not found.

##### Exceptions

- `Au.Types.AuWndException`:
    This variable is invalid (window not found, closed, etc).

#### Remarks

This function is used mostly with controls, but supports top-level windows too. Skips maximized/minimized windows and desktop.

* * *

## Overload 2

Gets a visible sibling control below this.

```
public wnd SiblingBelow(int distance, int xOffset = 5, bool topChild = false)
```

##### Parameters

- *distance*  (`int`):
    Vertical distance from the bottom of this control.
- *xOffset*  (`int`):
    Horizontal offset from the left of this control. If negative - to the left. Default 5.
- *topChild*  (`bool`):
    If at that point is a visible child of the sibling, get that child. Default `false`.

##### Returns

`Au.wnd`

`default(wnd)` if there is no sibling.

##### Exceptions

- `Au.Types.AuWndException`:
    This variable is invalid (window not found, closed, etc).

#### Remarks

This function is used mostly with controls, but supports top-level windows too.