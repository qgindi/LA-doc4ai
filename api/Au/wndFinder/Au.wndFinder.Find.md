# Method `Au.wndFinder.Find`

## Overload 1

Finds the specified window, like `Au.wnd.find`.

```
public wnd Find()
```

##### Returns

`Au.wnd`

If found, returns `Au.wndFinder.Result`, else `default(wnd)`.

#### Remarks

Functions `Find` and `Au.wndFinder.Exists` differ only in their return types.

* * *

## Overload 2

Finds the specified window, like `Au.wnd.find`. Can wait and throw `Au.Types.NotFoundException`.

```
public wnd Find(Seconds wait)
```

##### Parameters

- *wait*  (`Au.Types.Seconds`):
    The wait timeout, seconds. If 0, does not wait. If negative, does not throw exception when not found.

##### Returns

`Au.wnd`

If found, returns `Au.wndFinder.Result`. Else throws exception or returns `default(wnd)` (if *wait* negative).

##### Exceptions

- `Au.Types.NotFoundException`

#### Remarks

Functions `Find` and `Au.wndFinder.Exists` differ only in their return types.