# Method `Au.wnd.getwnd.Previous`

Gets previous sibling window or control in the Z order.

```
public wnd Previous(int skip = 0)
```

##### Parameters

- *skip*  (`int`):
    How many previous windows to skip.

##### Returns

`Au.wnd`

`default(wnd)` if this is the first or if failed.

#### Remarks

If this is a top-level window, gets previous top-level window, else gets previous control of the same direct parent. Calls API `GetWindow`(`GW_HWNDPREV`). Supports `Au.lastError`.