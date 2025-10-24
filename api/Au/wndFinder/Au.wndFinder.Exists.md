# Method `Au.wndFinder.Exists`

## Overload 1

Finds the specified window, like `Au.wnd.find`.

```
public bool Exists()
```

##### Returns

`bool`

If found, sets `Au.wndFinder.Result` and returns `true`, else `false`.

#### Remarks

Functions `Find` and `Au.wndFinder.Exists` differ only in their return types.

* * *

## Overload 2

Finds the specified window, like `Au.wnd.find`. Can wait and throw `Au.Types.NotFoundException`.

```
public bool Exists(Seconds wait)
```

##### Parameters

- *wait*  (`Au.Types.Seconds`):
    The wait timeout, seconds. If 0, does not wait. If negative, does not throw exception when not found.

##### Returns

`bool`

If found, sets `Au.wndFinder.Result` and returns `true`. Else throws exception or returns `false` (if *wait* negative).

##### Exceptions

- `Au.Types.NotFoundException`

#### Remarks

Functions `Find` and `Au.wndFinder.Exists` differ only in their return types.