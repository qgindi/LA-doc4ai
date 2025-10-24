# Method `Au.screen.isInAnyScreen`

## Overload 1

Returns `true` if point *p* is in some screen.

```
public static bool isInAnyScreen(POINT p)
```

##### Parameters

- *p*  (`Au.Types.POINT`)

##### Returns

`bool`

* * *

## Overload 2

Returns `true` if rectangle *r* intersects with some screen.

```
public static bool isInAnyScreen(RECT r)
```

##### Parameters

- *r*  (`Au.Types.RECT`)

##### Returns

`bool`

* * *

## Overload 3

Returns `true` if rectangle of window *w* intersects with some screen.

```
public static bool isInAnyScreen(wnd w)
```

##### Parameters

- *w*  (`Au.wnd`)

##### Returns

`bool`