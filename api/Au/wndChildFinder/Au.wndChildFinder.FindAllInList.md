# Method `Au.wndChildFinder.FindAllInList`

Finds all matching controls in a list of controls.

```
public wnd[] FindAllInList(IEnumerable<wnd> a, wnd wParent = default)
```

##### Parameters

- *a*  (`IEnumerable<Au.wnd>`):
    List of controls, for example returned by `Au.wnd.getwnd.Children`.
- *wParent*  (`Au.wnd`):
    Direct or indirect parent window. Used only for flag `DirectChild`.

##### Returns

`Au.wnd[]`

Array containing zero or more `Au.wnd`.