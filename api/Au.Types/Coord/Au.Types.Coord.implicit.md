# Operator `Au.Types.Coord.implicit operator`

## Overload 1

Creates `Au.Types.Coord` of `Normal` type.

```
public static implicit operator Coord(int v)
```

##### Parameters

- *v*  (`int`)

##### Returns

`Au.Types.Coord`

* * *

## Overload 2

Creates `Au.Types.Coord` of `Normal` or `Reverse` type. Reverse if the index is from end, like `^1`.

```
public static implicit operator Coord(Index v)
```

##### Parameters

- *v*  (`Index`)

##### Returns

`Au.Types.Coord`

* * *

## Overload 3

Creates `Au.Types.Coord` of `Fraction` type.

```
public static implicit operator Coord(float v)
```

##### Parameters

- *v*  (`float`)

##### Returns

`Au.Types.Coord`