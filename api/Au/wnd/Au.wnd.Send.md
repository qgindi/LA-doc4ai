# Method `Au.wnd.Send`

## Overload 1

Calls API `SendMessage`.

```
public nint Send(int message, nint wParam = 0, nint lParam = 0)
```

##### Parameters

- *message*  (`int`)
- *wParam*  (`nint`)
- *lParam*  (`nint`)

##### Returns

`nint`

#### Remarks

Supports `Au.lastError`.

* * *

## Overload 2

Calls API `SendMessage` where *lParam* is string.

```
public nint Send(int message, nint wParam, string lParam)
```

##### Parameters

- *message*  (`int`)
- *wParam*  (`nint`)
- *lParam*  (`string`)

##### Returns

`nint`

#### Remarks

Supports `Au.lastError`.

* * *

## Overload 3

Calls API `SendMessage` where *lParam* is any pointer.

```
public nint Send(int message, nint wParam, void* lParam)
```

##### Parameters

- *message*  (`int`)
- *wParam*  (`nint`)
- *lParam*  (`void*`)

##### Returns

`nint`

#### Remarks

Supports `Au.lastError`.