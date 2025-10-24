# Method `Au.wnd.MapWindowToClient`

## Overload 1

Converts coordinates relative to the top-left corner of this window to coordinates relative to the client area of this window.

```
public bool MapWindowToClient(ref POINT p)
```

##### Parameters

- *p*  (`Au.Types.POINT`)

##### Returns

`bool`

#### Remarks

Supports `Au.lastError`.

* * *

## Overload 2

Converts coordinates relative to the top-left corner of this window to coordinates relative to the client area of this window.

```
public bool MapWindowToClient(ref RECT r)
```

##### Parameters

- *r*  (`Au.Types.RECT`)

##### Returns

`bool`

#### Remarks

Supports `Au.lastError`.