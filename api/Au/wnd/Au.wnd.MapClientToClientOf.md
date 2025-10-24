# Method `Au.wnd.MapClientToClientOf`

## Overload 1

Converts coordinates relative to the client area of this window to coordinates relative to the client area of window *w*.

```
public bool MapClientToClientOf(wnd w, ref RECT r)
```

##### Parameters

- *w*  (`Au.wnd`)
- *r*  (`Au.Types.RECT`)

##### Returns

`bool`

#### Remarks

Supports `Au.lastError`.

* * *

## Overload 2

Converts coordinates relative to the client area of this window to coordinates relative to the client area of window *w*.

```
public bool MapClientToClientOf(wnd w, ref POINT p)
```

##### Parameters

- *w*  (`Au.wnd`)
- *p*  (`Au.Types.POINT`)

##### Returns

`bool`

#### Remarks

Supports `Au.lastError`.