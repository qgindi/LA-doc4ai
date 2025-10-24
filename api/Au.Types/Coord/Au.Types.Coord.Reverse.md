# Method `Au.Types.Coord.Reverse`

Creates `Au.Types.Coord` of `Reverse` type. Value 0 is at the right or bottom, and does not belong to the rectangle. Positive values are towards left or top.

```
public static Coord Reverse(int v)
```

##### Parameters

- *v*  (`int`)

##### Returns

`Au.Types.Coord`

#### Remarks

Instead can be use "from end" index, for example argument `Coord.Reverse(1)` can be replaced with `^1`.