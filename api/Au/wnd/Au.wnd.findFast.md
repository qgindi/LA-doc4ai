# Method `Au.wnd.findFast`

Finds a top-level window and returns its handle as `Au.wnd`.

```
public static wnd findFast(string name = null, string cn = null, bool messageOnly = false, wnd wAfter = default)
```

##### Parameters

- *name*  (`string`):
    Name. Full, case-insensitive. Wildcard etc not supported. `null` means "can be any". `""` means "no name".
- *cn*  (`string`):
    Class name. Full, case-insensitive. Wildcard etc not supported. `null` means "can be any". Cannot be `""`.
- *messageOnly*  (`bool`):
    Search only message-only windows.
- *wAfter*  (`Au.wnd`):
    If used, starts searching from the next window in the Z order.

##### Returns

`Au.wnd`

Returns `default(wnd)` if not found. See also: `Au.wnd.Is0`.

#### Remarks

Calls API `FindWindowEx`. Faster than `Au.wnd.find`, which uses API `EnumWindows`. Finds hidden windows too. Supports `Au.lastError`. It is not recommended to use this function in a loop to enumerate windows. It would be unreliable because window positions in the Z order can be changed while enumerating. Also then it would be slower than `Au.wnd.find` and `Au.wnd.findAll`.