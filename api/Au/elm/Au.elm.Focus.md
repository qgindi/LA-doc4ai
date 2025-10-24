# Method `Au.elm.Focus`

Makes this UI element focused for keyboard input.

```
public void Focus(bool andSelect = false)
```

##### Parameters

- *andSelect*  (`bool`):
    Add flag `TAKESELECTION`. Note: it is for selecting a list item, not for selecting text in a text box.

##### Exceptions

- `Au.Types.AuException`:
    Failed.
- `Au.Types.AuWndException`:
    Failed to activate the window (`Au.wnd.Activate`) or focus the control (`Au.wnd.Focus`).

#### Remarks

Calls `Au.elm.Select` with flag `TAKEFOCUS` and optionally `TAKESELECTION`. Not all UI elements support this action and not all work correctly. More info in `Select` documentation.