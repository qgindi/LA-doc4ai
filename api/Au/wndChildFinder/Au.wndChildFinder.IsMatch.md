# Method `Au.wndChildFinder.IsMatch`

Returns `true` if control `c` properties match the specified properties.

```
public bool IsMatch(wnd c, wnd wParent = default)
```

##### Parameters

- *c*  (`Au.wnd`):
    A control. Can be 0/invalid, then returns `false`.
- *wParent*  (`Au.wnd`):
    Direct or indirect parent window. If used, returns `false` if it isn't parent (also depends on flag `DirectChild`).

##### Returns

`bool`