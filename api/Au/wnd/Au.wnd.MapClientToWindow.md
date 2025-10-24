# Method `Au.wnd.MapClientToWindow`

## Overload 1

Converts coordinates relative to the client area of this window to coordinates relative to the top-left corner of this window.

```
public bool MapClientToWindow(ref POINT p)
```

##### Parameters

- *p*  (`Au.Types.POINT`)

##### Returns

`bool`

#### Remarks

Supports `Au.lastError`.

* * *

## Overload 2

Converts coordinates relative to the client area of this window to coordinates relative to the top-left corner of this window.

```
public bool MapClientToWindow(ref RECT r)
```

##### Parameters

- *r*  (`Au.Types.RECT`)

##### Returns

`bool`

#### Remarks

Supports `Au.lastError`.