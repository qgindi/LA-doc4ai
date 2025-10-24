# Method `Au.More.Math2.Distance`

## Overload 1

Calculates distance between two points.

```
public static double Distance(POINT p1, POINT p2)
```

##### Parameters

- *p1*  (`Au.Types.POINT`)
- *p2*  (`Au.Types.POINT`)

##### Returns

`double`

* * *

## Overload 2

Calculates distance between rectangle and point.

```
public static double Distance(RECT r, POINT p)
```

##### Parameters

- *r*  (`Au.Types.RECT`)
- *p*  (`Au.Types.POINT`)

##### Returns

`double`

If the point is outside, returns the nearest distance, else 0.