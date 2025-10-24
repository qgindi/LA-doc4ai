# Method `Au.Types.RECT.Intersect`

## Overload 1

Replaces this rectangle with the intersection of itself and the specified rectangle. If the rectangles don't intersect, makes this variable empty.

```
public bool Intersect(RECT r2)
```

##### Parameters

- *r2*  (`Au.Types.RECT`)

##### Returns

`bool`

`true` if the rectangles intersect.

* * *

## Overload 2

Returns the intersection rectangle of two rectangles. If they don't intersect, returns empty rectangle.

```
public static RECT Intersect(RECT r1, RECT r2)
```

##### Parameters

- *r1*  (`Au.Types.RECT`)
- *r2*  (`Au.Types.RECT`)

##### Returns

`Au.Types.RECT`