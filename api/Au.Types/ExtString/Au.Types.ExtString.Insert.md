# Method `Au.Types.ExtString.Insert`

Inserts other string.

```
public static string Insert(this string t, Index startIndex, string s)
```

##### Parameters

- *t*  (`string`):
    This string.
- *startIndex*  (`Index`):
    Offset in this string. Can be from end, like `^4`.
- *s*  (`string`):
    String to insert.

##### Returns

`string`

The result string.

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *startIndex*.