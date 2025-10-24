# Method `Au.wndFinder.IsMatch`

Returns `true` if window *w* properties match the specified properties.

```
public bool IsMatch(wnd w, WFCache cache = null)
```

##### Parameters

- *w*  (`Au.wnd`):
    A top-level window. If 0 or invalid, returns `false`.
- *cache*  (`Au.Types.WFCache`):
    Can be used to make faster when multiple `Au.wndFinder` variables are used with same window. The function gets window name/class/program once, and stores in *cache*; next time it gets these strings from *cache*.

##### Returns

`bool`

### See Also

`Au.wnd.IsMatch`