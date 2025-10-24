# Method `Au.wnd.getwnd.LastActiveOwnedOrThis`

Gets the most recently active window in the chain of windows owned by this window, or this window itself if there are no such windows.

```
public wnd LastActiveOwnedOrThis(bool includeOwners = false)
```

##### Parameters

- *includeOwners*  (`bool`):
    Can return an owner (or owner's owner and so on) of this window too.

##### Returns

`Au.wnd`

`default(wnd)` if failed.

#### Remarks

Supports `Au.lastError`.