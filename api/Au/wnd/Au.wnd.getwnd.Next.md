# Method `Au.wnd.getwnd.Next`

Gets next sibling window or control in the Z order.

```
public wnd Next(int skip = 0)
```

##### Parameters

- *skip*  (`int`):
    How many next windows to skip.

##### Returns

`Au.wnd`

`default(wnd)` if this is the last or if failed.

#### Remarks

If this is a top-level window, gets next top-level window, else gets next control of the same direct parent. Calls API `GetWindow`(`GW_HWNDNEXT`). Supports `Au.lastError`.