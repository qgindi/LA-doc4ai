# Operator `Au.Types.WOwner.implicit operator`

## Overload 1

Program name like `"notepad.exe"`, or `null`. See `Au.wnd.ProgramName`.

```
public static implicit operator WOwner(string program)
```

##### Parameters

- *program*  (`string`)

##### Returns

`Au.Types.WOwner`

* * *

## Overload 2

Owner window. See `Au.wnd.getwnd.Owner`. Will use `Au.wnd.IsOwnedBy` with level 2.

```
public static implicit operator WOwner(wnd ownerWindow)
```

##### Parameters

- *ownerWindow*  (`Au.wnd`)

##### Returns

`Au.Types.WOwner`