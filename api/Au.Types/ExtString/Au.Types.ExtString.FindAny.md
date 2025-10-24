# Method `Au.Types.ExtString.FindAny`

Finds the first character specified in *chars*. Returns its index, or -1 if not found.

```
public static int FindAny(this string t, string chars, Range? range = null)
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