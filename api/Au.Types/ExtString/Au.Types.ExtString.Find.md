# Method `Au.Types.ExtString.Find`

## Overload 1

Finds substring in this string. Returns its 0-based index, or -1 if not found.

```
public static int Find(this string t, string s, bool ignoreCase = false)
```

##### Parameters

- *t*  (`string`):
    This string.
- *s*  (`string`):
    Substring to find.
- *ignoreCase*  (`bool`):
    Case-insensitive.

##### Returns

`int`

##### Exceptions

- `ArgumentNullException`:
    *s* is `null`.

#### Remarks

Uses ordinal comparison (does not depend on current culture/locale).

* * *

## Overload 2

Finds substring in part of this string. Returns its 0-based index, or -1 if not found.

```
public static int Find(this string t, string s, int startIndex, bool ignoreCase = false)
```

##### Parameters

- *t*  (`string`):
    This string.
- *s*  (`string`):
    Substring to find.
- *startIndex*  (`int`):
    The search start index.
- *ignoreCase*  (`bool`):
    Case-insensitive.

##### Returns

`int`

##### Exceptions

- `ArgumentNullException`:
    *s* is `null`.
- `ArgumentOutOfRangeException`:
    Invalid *startIndex*.

#### Remarks

Uses ordinal comparison (does not depend on current culture/locale).

* * *

## Overload 3

Finds substring in part of this string. Returns its 0-based index, or -1 if not found.

```
public static int Find(this string t, string s, Range range, bool ignoreCase = false)
```

##### Parameters

- *t*  (`string`):
    This string.
- *s*  (`string`):
    Substring to find.
- *range*  (`Range`):
    The search range.
- *ignoreCase*  (`bool`):
    Case-insensitive.

##### Returns

`int`

##### Exceptions

- `ArgumentNullException`:
    *s* is `null`.
- `ArgumentOutOfRangeException`:
    Invalid *range*.

#### Remarks

Uses ordinal comparison (does not depend on current culture/locale).