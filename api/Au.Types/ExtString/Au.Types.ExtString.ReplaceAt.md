# Method `Au.Types.ExtString.ReplaceAt`

## Overload 1

Replaces part of this string with other string.

```
public static string ReplaceAt(this string t, int startIndex, int count, string s)
```

##### Parameters

- *t*  (`string`):
    This string.
- *startIndex*  (`int`):
    Offset in this string.
- *count*  (`int`):
    Count of characters to replace.
- *s*  (`string`):
    The replacement string.

##### Returns

`string`

The result string.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *startIndex* or *count*.

* * *

## Overload 2

Replaces part of this string with other string.

```
public static string ReplaceAt(this string t, Range range, string s)
```

##### Parameters

- *t*  (`string`):
    This string.
- *range*  (`Range`):
    Part of this string to replace.
- *s*  (`string`):
    The replacement string.

##### Returns

`string`

The result string.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *range*.