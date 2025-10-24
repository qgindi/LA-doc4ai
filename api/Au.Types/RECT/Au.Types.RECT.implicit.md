# Operator `Au.Types.RECT.implicit operator`

## Overload 1

Converts from tuple (left, top, width, height).

```
public static implicit operator RECT((int L, int T, int W, int H) t)
```

##### Parameters

- *t*  (`(int L, int T, int W, int H)`)

##### Returns

`Au.Types.RECT`

* * *

## Overload 2

```
public static implicit operator RECT(Rectangle r)
```

##### Parameters

- *r*  (`Rectangle`)

##### Returns

`Au.Types.RECT`

* * *

## Overload 3

```
public static implicit operator Rectangle(RECT r)
```

##### Parameters

- *r*  (`Au.Types.RECT`)

##### Returns

`Rectangle`

* * *

## Overload 4

```
public static implicit operator RectangleF(RECT r)
```

##### Parameters

- *r*  (`Au.Types.RECT`)

##### Returns

`RectangleF`

* * *

## Overload 5

```
public static implicit operator Rect(RECT r)
```

##### Parameters

- *r*  (`Au.Types.RECT`)

##### Returns

`Rect`