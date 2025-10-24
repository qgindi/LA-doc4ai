# Method `Au.wnd.getwnd.AllOwners`

Gets all owner windows (owner, its owner and so on) of this window.

```
public wnd[] AllOwners(bool andThisWindow = false, bool onlyVisible = false)
```

##### Parameters

- *andThisWindow*  (`bool`):
    Add this window (or its top-level parent if control) as the first list element.
- *onlyVisible*  (`bool`):
    Skip invisible windows.

##### Returns

`Au.wnd[]`

#### Remarks

This window can be top-level window or control.