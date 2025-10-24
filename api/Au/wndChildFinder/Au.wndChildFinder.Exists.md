# Method `Au.wndChildFinder.Exists`

## Overload 1

Finds the specified child control, like `Au.wnd.Child`.

```
public bool Exists(wnd wParent)
```

##### Parameters

- *wParent*  (`Au.wnd`):
    Direct or indirect parent window. Can be top-level window or control.

##### Returns

`bool`

If found, sets `Au.wndChildFinder.Result` and returns `true`, else `false`.

##### Exceptions

- `Au.Types.AuWndException`:
    Invalid *wParent*.

#### Remarks

Functions `Find` and `Au.wndChildFinder.Exists(wnd)` differ only in their return types.

* * *

## Overload 2

Finds the specified child control, like `Au.wnd.Child`. Can wait and throw `Au.Types.NotFoundException`.

```
public bool Exists(wnd wParent, Seconds wait)
```

##### Parameters

- *wParent*  (`Au.wnd`):
    Direct or indirect parent window. Can be top-level window or control.
- *wait*  (`Au.Types.Seconds`):
    The wait timeout, seconds. If 0, does not wait. If negative, does not throw exception when not found.

##### Returns

`bool`

If found, sets `Au.wndChildFinder.Result` and returns `true`. Else throws exception or returns `false` (if *wait* negative).

##### Exceptions

- `Au.Types.AuWndException`:
    Invalid *wParent*.
- `Au.Types.NotFoundException`

#### Remarks

Functions `Find` and `Au.wndChildFinder.Exists(wnd)` differ only in their return types.