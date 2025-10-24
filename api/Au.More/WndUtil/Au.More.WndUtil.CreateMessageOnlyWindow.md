# Method `Au.More.WndUtil.CreateMessageOnlyWindow`

## Overload 1

Creates native/unmanaged [message-only window](https://www.google.com/search?q=message-only+window+site:microsoft.com).

```
public static wnd CreateMessageOnlyWindow(string className, string name = null)
```

##### Parameters

- *className*  (`string`):
    Window class name. Can be any existing class.
- *name*  (`string`):
    Window name or `null`.

##### Returns

`Au.wnd`

##### Exceptions

- `Au.Types.AuException`:
    Failed to create window. Unlikely.

#### Remarks

Styles: `WS_POPUP`, `WS_EX_NOACTIVATE`. To destroy the window can be used any function, including API `DestroyWindow`, `Au.More.WndUtil.DestroyWindow`, `Au.wnd.Close`, API `WM_CLOSE`.

* * *

## Overload 2

Creates native/unmanaged [message-only window](https://www.google.com/search?q=message-only+window+site:microsoft.com) and sets its window procedure.

```
public static wnd CreateMessageOnlyWindow(WNDPROC wndProc, string className, string name = null)
```

##### Parameters

- *wndProc*  (`Au.Types.WNDPROC`)
- *className*  (`string`):
    Window class name.
- *name*  (`string`):
    Window name or `null`.

##### Returns

`Au.wnd`

##### Exceptions

- `Au.Types.AuException`:
    Failed to create window. Unlikely.

#### Remarks

Styles: `WS_POPUP`, `WS_EX_NOACTIVATE`. Calls `Au.More.WndUtil.CreateWindow` with *keepAlive*=`true`.