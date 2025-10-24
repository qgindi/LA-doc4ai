# Method `Au.Types.ExtMisc.InsertAt`

## Overload 1

Creates a copy of this array with one inserted element.

```
public static T[] InsertAt<T>(this T[] t, int index, T value = default)
```

##### Parameters

- *t*  (`T[]`)
- *index*  (`int`):
    Where to insert. If -1, adds to the end.
- *value*  (`T`)

##### Returns

`T[]`

##### Exceptions

- `ArgumentOutOfRangeException`

##### Type Parameters

- `T`

* * *

## Overload 2

Creates a copy of this array with several inserted elements.

```
public static T[] InsertAt<T>(this T[] t, int index, params ReadOnlySpan<T> values)
```

##### Parameters

- *t*  (`T[]`)
- *index*  (`int`):
    Where to insert. If -1, adds to the end.
- *values*  (`ReadOnlySpan<T>`)

##### Returns

`T[]`

##### Exceptions

- `ArgumentOutOfRangeException`

##### Type Parameters

- `T`