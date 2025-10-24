# Method `Au.wnd.Post`

Calls/returns API `PostMessage`.

```
public bool Post(int message, nint wParam = 0, nint lParam = 0)
```

##### Parameters

- *message*  (`int`)
- *wParam*  (`nint`)
- *lParam*  (`nint`)

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.

### See Also

`Au.More.WndUtil.PostThreadMessage`