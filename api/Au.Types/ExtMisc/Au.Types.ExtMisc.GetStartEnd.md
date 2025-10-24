# Method `Au.Types.ExtMisc.GetStartEnd`

## Overload 1

Calls `System.Range.GetOffsetAndLength` and returns start and end instead of start and length.

```
public static (int start, int end) GetStartEnd(this Range t, int length)
```

##### Parameters

- *t*  (`Range`)
- *length*  (`int`)

##### Returns

`(int start, int end)`

##### Exceptions

- `ArgumentOutOfRangeException`

* * *

## Overload 2

If this is `null`, returns `(0, length)`. Else calls `System.Range.GetOffsetAndLength` and returns start and end instead of start and length.

```
public static (int start, int end) GetStartEnd(this Range? t, int length)
```

##### Parameters

- *t*  (`Range?`)
- *length*  (`int`)

##### Returns

`(int start, int end)`

##### Exceptions

- `ArgumentOutOfRangeException`