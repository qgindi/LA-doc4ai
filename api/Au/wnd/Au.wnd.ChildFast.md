# Method `Au.wnd.ChildFast`

## Overload 1

Finds a direct child control by name and/or class name and returns its handle as `Au.wnd`.

```
public wnd ChildFast(string name, string cn, wnd wAfter = default)
```

##### Parameters

- *name*  (`string`):
    Name. Full, case-insensitive. Wildcard etc not supported. `null` means "can be any". `""` means "no name". Must include the invisible `'&'` characters that are used to underline keyboard shortcuts with the `Alt` key.
- *cn*  (`string`):
    Class name. Full, case-insensitive. Wildcard etc not supported. `null` means "can be any". Cannot be `""`.
- *wAfter*  (`Au.wnd`):
    If used, starts searching from the next control in the Z order.

##### Returns

`Au.wnd`

Returns `default(wnd)` if not found. See also: `Au.wnd.Is0`. Supports `Au.lastError`.

#### Remarks

Calls API `FindWindowEx`. Faster than `Au.wnd.Child`, which uses API `EnumChildWindows`. Can be used only when you know full name and/or class name. Finds hidden controls too. Finds only direct children, not other descendants.

* * *

## Overload 2

Finds a direct child control by its id and returns its handle as `Au.wnd`.

```
public wnd ChildFast(int id)
```

##### Parameters

- *id*  (`int`):
    Control id.

##### Returns

`Au.wnd`

Returns `default(wnd)` if not found. See also: `Au.wnd.Is0`. Supports `Au.lastError`.

#### Remarks

Calls API `GetDlgItem`. Faster than `Au.wnd.Child`, which uses API `EnumChildWindows`. Finds only direct children, not other descendants. Finds hidden controls too. Not all controls have a useful id. If control id is not unique or is different in each window instance, this function is not useful.