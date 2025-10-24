# Method `Au.wnd.SendNotify`

Calls/returns API `SendNotifyMessage`.

```
public bool SendNotify(int message, nint wParam = 0, nint lParam = 0)
```

##### Parameters

- *message*  (`int`)
- *wParam*  (`nint`)
- *lParam*  (`nint`)

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.