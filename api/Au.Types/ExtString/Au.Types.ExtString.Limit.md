# Method `Au.Types.ExtString.Limit`

If this string is longer than *limit*, returns its substring 0 to *limit*-1 with appended `'…'` character. Else returns this string.

```
public static string Limit(this string t, int limit, bool middle = false, bool lines = false)
```

##### Parameters

- *t*  (`string`):
    This string.
- *limit*  (`int`):
    Maximal length of the result string. If less than 1, uses 1.
- *middle*  (`bool`):
    Let `"…"` be in the middle. For example it is useful when the string is a file path, to avoid removing the filename.
- *lines*  (`bool`):
    *limit* is lines, not characters.

##### Returns

`string`