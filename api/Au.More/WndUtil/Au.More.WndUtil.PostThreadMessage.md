# Method `Au.More.WndUtil.PostThreadMessage`

Calls API `PostThreadMessage`.

```
public static bool PostThreadMessage(int threadId, int message, nint wParam = 0, nint lParam = 0)
```

##### Parameters

- *threadId*  (`int`)
- *message*  (`int`)
- *wParam*  (`nint`)
- *lParam*  (`nint`)

##### Returns

`bool`

`false` if failed. Supports `Au.lastError`.