# Operator `Au.Types.StartEnd.implicit operator`

## Overload 1

```
public static implicit operator Range(StartEnd s)
```

##### Parameters

- *s*  (`Au.Types.StartEnd`)

##### Returns

`Range`

* * *

## Overload 2

```
public static implicit operator StartEnd(Range r)
```

##### Parameters

- *r*  (`Range`)

##### Returns

`Au.Types.StartEnd`

##### Exceptions

- `ArgumentException`:
    The start or end of the range is from the end.