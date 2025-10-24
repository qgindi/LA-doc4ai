# Method `Au.Types.ExtString.FindLastNot`

Finds the last character not specified in *chars* (searches right to left). Returns its index, or -1 if not found.

```
public static int FindLastNot(this string t, string chars, Range? range = null)
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