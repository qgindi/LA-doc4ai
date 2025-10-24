# Method `Au.wndChildFinder.FindInList`

Finds the specified control in a list of controls. The `Au.wndChildFinder.Result` property will be the control.

```
public int FindInList(IEnumerable<wnd> a, wnd wParent = default)
```

##### Parameters

- *a*  (`IEnumerable<Au.wnd>`):
    List of controls, for example returned by `Au.wnd.getwnd.Children`.
- *wParent*  (`Au.wnd`):
    Direct or indirect parent window. Used only for flag `DirectChild`.

##### Returns

`int`

0-based index, or -1 if not found.