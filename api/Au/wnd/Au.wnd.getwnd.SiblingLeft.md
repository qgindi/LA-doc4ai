# Method `Au.wnd.getwnd.SiblingLeft`

## Overload 1

Gets nearest visible sibling control to the left from this.

```
public wnd SiblingLeft()
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

Gets a visible sibling control to the left from this.

```
public wnd SiblingLeft(int distance, int yOffset = 5, bool topChild = false)
```

##### Parameters

- *distance*  (`int`):
    Horizontal distance from the left of this control.
- *yOffset*  (`int`):
    Vertical offset from the top of this control. If negative - up. Default 5.
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