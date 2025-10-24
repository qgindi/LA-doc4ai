# Method `Au.print.list`

## Overload 1

Writes an array or generic collection to the output, as a list of items separated by *separator*.

```
public static void list<T>(string separator, IEnumerable<T> value)
```

##### Parameters

- *separator*  (`string`)
- *value*  (`IEnumerable<T>`):
    Array or generic collection of any type. If `null`, writes `"null"`.

##### Type Parameters

- `T`

* * *

## Overload 2

Writes multiple arguments of any type to the output, using *separator*.

```
public static void list(string separator, object value1, object value2, params object[] more)
```

##### Parameters

- *separator*  (`string`)
- *value1*  (`object`)
- *value2*  (`object`)
- *more*  (`object[]`)

#### Remarks

If a value is `null`, writes `"null"`. If a value is unsigned integer (`uint`, `ulong`, `ushort`, `byte`, `nuint`), writes in hexadecimal format with prefix `"0x"`.