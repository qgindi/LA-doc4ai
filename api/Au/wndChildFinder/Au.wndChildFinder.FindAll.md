# Method `Au.wndChildFinder.FindAll`

Finds all matching child controls, like `Au.wnd.ChildAll`.

```
public wnd[] FindAll(wnd wParent)
```

##### Parameters

- *wParent*  (`Au.wnd`):
    Direct or indirect parent window. Can be top-level window or control.

##### Returns

`Au.wnd[]`

Array containing zero or more `Au.wnd`.

##### Exceptions

- `Au.Types.AuWndException`:
    Invalid *wParent*.