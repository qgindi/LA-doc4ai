# Method `Au.Types.RECT.Union`

## Overload 1

Replaces this rectangle with the union of itself and the specified rectangle. Union is the smallest rectangle that contains two full rectangles.

```
public bool Union(RECT r2)
```

##### Parameters

- *r2*  (`Au.Types.RECT`)

##### Returns

`bool`

`true` if finally this rectangle is not empty.

#### Remarks

If either rectangle is empty (`Au.Types.RECT.Width` or `Au.Types.RECT.Height` is \<=0), the result is another rectangle. If both empty - empty rectangle.

* * *

## Overload 2

Returns the union of two rectangles. Union is the smallest rectangle that contains two full rectangles.

```
public static RECT Union(RECT r1, RECT r2)
```

##### Parameters

- *r1*  (`Au.Types.RECT`)
- *r2*  (`Au.Types.RECT`)

##### Returns

`Au.Types.RECT`

#### Remarks

If either rectangle is empty (`Au.Types.RECT.Width` or `Au.Types.RECT.Height` is \<=0), the result is another rectangle. If both empty - empty rectangle.