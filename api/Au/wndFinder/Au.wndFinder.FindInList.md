# Method `Au.wndFinder.FindInList`

Finds the specified window in a list of windows, and sets `Au.wndFinder.Result`.

```
public int FindInList(IEnumerable<wnd> a)
```

##### Parameters

- *a*  (`IEnumerable<Au.wnd>`):
    Array or list of windows, for example returned by `Au.wnd.getwnd.allWindows`.

##### Returns

`int`

Returns 0-based index, or -1 if not found.