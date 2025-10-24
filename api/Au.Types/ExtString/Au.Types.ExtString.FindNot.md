# Method `Au.Types.ExtString.FindNot`

Finds the first character not specified in *chars*. Returns its index, or -1 if not found.

```
public static int FindNot(this string t, string chars, Range? range = null)
```

##### Parameters

- *t*  (`string`):
    This string.
- *chars*  (`string`):
    Characters.
- *range*  (`Range?`):
    The search range.

##### Returns

`int`

##### Exceptions

- `ArgumentNullException`:
    *chars* is `null`.
- `ArgumentOutOfRangeException`:
    Invalid *range*.