# Method `Au.wnd.HasStyle`

Returns `true` if the window has all specified style flags (see `Au.wnd.Style`).

```
public bool HasStyle(WS style, bool any = false)
```

##### Parameters

- *style*  (`Au.Types.WS`):
    One or more styles.
- *any*  (`bool`):
    Return `true` if has any (not necessary all) of the specified styles. Note: don't use `Au.Types.WS.CAPTION`, because it consists of two other styles - `BORDER` and `DLGFRAME`.

##### Returns

`bool`

#### Remarks

Supports `Au.lastError`.