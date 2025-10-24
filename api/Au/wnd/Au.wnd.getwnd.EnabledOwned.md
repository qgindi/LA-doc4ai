# Method `Au.wnd.getwnd.EnabledOwned`

Gets the first (in Z order) enabled window owned by this window.

```
public wnd EnabledOwned(bool orThis = false)
```

##### Parameters

- *orThis*  (`bool`):
    Return this window if there are no enabled owned windows. If `false`, then returns `default(wnd)`.

##### Returns

`Au.wnd`

#### Remarks

This window should be top-level, not child; see `Au.wnd.Window`.

Calls API `GetWindow`(`GW_ENABLEDPOPUP`). Supports `Au.lastError`.