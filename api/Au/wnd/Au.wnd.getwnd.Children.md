# Method `Au.wnd.getwnd.Children`

Gets child controls, including all descendants.

```
public wnd[] Children(bool onlyVisible = false, bool sortFirstVisible = false, bool directChild = false)
```

##### Parameters

- *onlyVisible*  (`bool`):
    Need only visible controls.
- *sortFirstVisible*  (`bool`):
    Place all array elements of hidden controls at the end of the array.
- *directChild*  (`bool`):
    Need only direct children, not all descendants.

##### Returns

`Au.wnd[]`

Array containing zero or more `Au.wnd`.

##### Exceptions

- `Au.Types.AuWndException`:
    This variable is invalid (window not found, closed, etc).

#### Remarks

Calls API `EnumChildWindows`.

### See Also

`Au.wnd.ChildAll`