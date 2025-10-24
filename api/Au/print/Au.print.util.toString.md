# Method `Au.print.util.toString`

## Overload 1

Converts value of any type to `string`. Formats it like `Au.print.it`.

```
public static string toString(object value, bool compact = false)
```

##### Parameters

- *value*  (`object`):
    Value of any type. If `null`, returns `"null"`.
- *compact*  (`bool`):
    If *value* is `System.Collections.IEnumerable` or `System.Collections.DictionaryEntry`, format it like `"{ item1, item2 }"`.

##### Returns

`string`

* * *

## Overload 2

Appends value of any type to `StringBuilder`. Formats it like `Au.print.it`.

```
public static void toString(StringBuilder b, object value, bool compact)
```

##### Parameters

- *b*  (`StringBuilder`)
- *value*  (`object`):
    Value of any type. If `null`, returns `"null"`.
- *compact*  (`bool`):
    If *value* is `System.Collections.IEnumerable` or `System.Collections.DictionaryEntry`, format it like `"{ item1, item2 }"`.

* * *

## Overload 3

Converts binary data to a hexadecimal + characters string, similar to the format used in hex editors.

```
public static string toString(ReadOnlySpan<byte> data, int columns)
```

##### Parameters

- *data*  (`ReadOnlySpan<byte>`)
- *columns*  (`int`):
    The number of bytes in a row.

##### Returns

`string`