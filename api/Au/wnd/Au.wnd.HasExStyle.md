# Method `Au.wnd.HasExStyle`

Returns `true` if the window has all specified extended style flags (see `Au.wnd.ExStyle`).

```
public bool HasExStyle(WSE exStyle, bool any = false)
```

##### Parameters

- *exStyle*  (`Au.Types.WSE`):
    One or more extended styles.
- *any*  (`bool`):
    Return `true` if has any (not necessary all) of the specified styles.

##### Returns

`bool`

#### Remarks

Supports `Au.lastError`.