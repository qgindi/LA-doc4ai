# Method `Au.wnd.MapWindowToScreen`

## Overload 1

Converts coordinates relative to the top-left corner of this window to screen coordinates.

```
public bool MapWindowToScreen(ref POINT p)
```

##### Parameters

- *p*  (`Au.Types.POINT`)

##### Returns

`bool`

#### Remarks

Supports `Au.lastError`.

* * *

## Overload 2

Converts coordinates relative to the top-left corner of this window to screen coordinates.

```
public bool MapWindowToScreen(ref RECT r)
```

##### Parameters

- *r*  (`Au.Types.RECT`)

##### Returns

`bool`

#### Remarks

Supports `Au.lastError`.