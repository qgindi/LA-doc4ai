# Method `Au.wnd.getwnd.AllOwned`

Gets windows owned by this window.

```
public wnd[] AllOwned(bool allDescendants, bool andThisWindow = false)
```

##### Parameters

- *allDescendants*  (`bool`):
    Also get indirectly owned windows (owned by owned windows).
- *andThisWindow*  (`bool`):
    Add this window to the array. Since the array is sorted like in the Z order, usually it is the last element, but not always.

##### Returns

`Au.wnd[]`

Array containing zero or more elements. Sorted like in the Z order.