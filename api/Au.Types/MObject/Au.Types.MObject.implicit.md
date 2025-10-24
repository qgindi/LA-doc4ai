# Operator `Au.Types.MObject.implicit operator`

## Overload 1

Allows to specify coordinates in the client area of a window or control.

```
public static implicit operator MObject(wnd w)
```

##### Parameters

- *w*  (`Au.wnd`)

##### Returns

`Au.Types.MObject`

##### Exceptions

- `Au.Types.AuWndException`:
    The window handle is 0.

### See Also

`Au.Types.MObject.Window`

* * *

## Overload 2

Allows to specify coordinates in the rectangle of a UI element.

```
public static implicit operator MObject(elm e)
```

##### Parameters

- *e*  (`Au.elm`)

##### Returns

`Au.Types.MObject`

##### Exceptions

- `ArgumentNullException`

* * *

## Overload 3

Allows to specify coordinates in the rectangle of an image found in a window etc.

```
public static implicit operator MObject(uiimage i)
```

##### Parameters

- *i*  (`Au.uiimage`)

##### Returns

`Au.Types.MObject`

##### Exceptions

- `ArgumentNullException`

* * *

## Overload 4

Allows to specify coordinates in a rectangle anywhere on screen.

```
public static implicit operator MObject(RECT r)
```

##### Parameters

- *r*  (`Au.Types.RECT`)

##### Returns

`Au.Types.MObject`

### See Also

`Au.Types.MObject.RectInWindow`

* * *

## Overload 5

Allows to specify coordinates in a screen.

```
public static implicit operator MObject(screen s)
```

##### Parameters

- *s*  (`Au.screen`)

##### Returns

`Au.Types.MObject`

### See Also

`Au.Types.MObject.Screen`

* * *

## Overload 6

Allows to specify coordinates relative to `Au.mouse.xy` or `Au.mouse.lastXY`.

```
public static implicit operator MObject(bool useLastXY)
```

##### Parameters

- *useLastXY*  (`bool`)

##### Returns

`Au.Types.MObject`