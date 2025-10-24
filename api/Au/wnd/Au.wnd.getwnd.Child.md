# Method `Au.wnd.getwnd.Child`

Gets a direct child control by index.

```
public wnd Child(int index)
```

##### Parameters

- *index*  (`int`):
    0-based index of the child control in the Z order.

##### Returns

`Au.wnd`

`default(wnd)` if no children or if index is invalid or if failed.

#### Remarks

Calls API `GetWindow`. Supports `Au.lastError`.