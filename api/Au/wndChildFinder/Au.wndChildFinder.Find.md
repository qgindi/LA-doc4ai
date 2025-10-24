# Method `Au.wndChildFinder.Find`

## Overload 1

Finds the specified child control, like `Au.wnd.Child`.

```
public wnd Find(wnd wParent)
```

##### Parameters

- *wParent*  (`Au.wnd`):
    Direct or indirect parent window. Can be top-level window or control.

##### Returns

`Au.wnd`

If found, returns `Au.wndChildFinder.Result`, else `default(wnd)`.

##### Exceptions

- `Au.Types.AuWndException`:
    Invalid *wParent*.

#### Remarks

Functions `Find` and `Au.wndChildFinder.Exists` differ only in their return types.

* * *

## Overload 2

Finds the specified child control, like `Au.wnd.Child`. Can wait and throw `Au.Types.NotFoundException`.

```
public wnd Find(wnd wParent, Seconds wait)
```

##### Parameters

- *wParent*  (`Au.wnd`):
    Direct or indirect parent window. Can be top-level window or control.
- *wait*  (`Au.Types.Seconds`):
    The wait timeout, seconds. If 0, does not wait. If negative, does not throw exception when not found.

##### Returns

`Au.wnd`

If found, returns `Au.wndChildFinder.Result`. Else throws exception or returns `default(wnd)` (if *wait* negative).

##### Exceptions

- `Au.Types.AuWndException`:
    Invalid *wParent*.
- `Au.Types.NotFoundException`

#### Remarks

Functions `Find` and `Au.wndChildFinder.Exists` differ only in their return types.