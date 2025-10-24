# Method `Au.Types.ExtString.FindLastAny`

Finds the last character specified in *chars* (searches right to left). Returns its index, or -1 if not found.

```
public static int FindLastAny(this string t, string chars, Range? range = null)
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