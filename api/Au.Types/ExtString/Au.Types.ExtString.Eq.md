# Method `Au.Types.ExtString.Eq`

## Overload 1

Compares this and other string. Returns `true` if equal.

```
public static bool Eq(this string t, string s, bool ignoreCase = false)
```

##### Parameters

- *t*  (`string`):
    This string. Can be `null`.
- *s*  (`string`):
    Other string. Can be `null`.
- *ignoreCase*  (`bool`):
    Case-insensitive.

##### Returns

`bool`

#### Remarks

Uses ordinal comparison (does not depend on current culture/locale).

### See Also

`Au.Types.ExtString.Eq(ReadOnlySpan<char>, ReadOnlySpan<char>)`

`Au.Types.ExtString.Eqi`

`string.Compare`

`string.CompareOrdinal`

* * *

## Overload 2

Compares this strings with multiple strings. Returns 1-based index of the matching string, or 0 if none.

```
public static int Eq(this string t, bool ignoreCase, params ReadOnlySpan<string> strings)
```

##### Parameters

- *t*  (`string`):
    This string. Can be `null`.
- *ignoreCase*  (`bool`):
    Case-insensitive.
- *strings*  (`ReadOnlySpan<string>`):
    Other strings. Strings can be `null`.

##### Returns

`int`

#### Remarks

Uses ordinal comparison (does not depend on current culture/locale).

* * *

## Overload 3

Compares part of this string with other string. Returns `true` if equal.

```
public static bool Eq(this string t, int startIndex, ReadOnlySpan<char> s, bool ignoreCase = false)
```

##### Parameters

- *t*  (`string`):
    This string.
- *startIndex*  (`int`):
    Offset in this string. If invalid, returns `false`.
- *s*  (`ReadOnlySpan<char>`):
    Other string.
- *ignoreCase*  (`bool`):
    Case-insensitive.

##### Returns

`bool`

##### Exceptions

- `ArgumentNullException`:
    *s* is `null`.

#### Remarks

Uses ordinal comparison (does not depend on current culture/locale).

### See Also

`Au.Types.ExtString.Eq(ReadOnlySpan<char>, int, ReadOnlySpan<char>, bool)`

`string.Compare`

`string.CompareOrdinal`

* * *

## Overload 4

Compares part of this string with multiple strings. Returns 1-based index of the matching string, or 0 if none.

```
public static int Eq(this string t, int startIndex, bool ignoreCase = false, params ReadOnlySpan<string> strings)
```

##### Parameters

- *t*  (`string`):
    This string.
- *startIndex*  (`int`):
    Offset in this string. If invalid, returns `false`.
- *ignoreCase*  (`bool`):
    Case-insensitive.
- *strings*  (`ReadOnlySpan<string>`):
    Other strings.

##### Returns

`int`

##### Exceptions

- `ArgumentNullException`:
    A string in *strings* is `null`.

#### Remarks

Uses ordinal comparison (does not depend on current culture/locale).

* * *

## Overload 5

Compares part of this string with other string. Returns `true` if equal.

```
public static bool Eq(this string t, Range range, ReadOnlySpan<char> s, bool ignoreCase = false)
```

##### Parameters

- *t*  (`string`):
    This string.
- *range*  (`Range`):
    Range of this string. Can return `true` only if its length `== s.Length`. If invalid, returns `false`.
- *s*  (`ReadOnlySpan<char>`):
    Other string.
- *ignoreCase*  (`bool`):
    Case-insensitive.

##### Returns

`bool`

##### Exceptions

- `ArgumentNullException`:
    *s* is `null`.

#### Remarks

Uses ordinal comparison (does not depend on current culture/locale).

### See Also

`Au.Types.ExtString.Eq(ReadOnlySpan<char>, ReadOnlySpan<char>)`

`Au.Types.ExtString.Eqi`

`string.Compare`

`string.CompareOrdinal`

* * *

## Overload 6

Returns `true` if the specified character is at the specified position in this string.

```
public static bool Eq(this string t, int index, char c)
```

##### Parameters

- *t*  (`string`):
    This string.
- *index*  (`int`):
    Offset in this string. If invalid, returns `false`.
- *c*  (`char`):
    Character.

##### Returns

`bool`

* * *

## Overload 7

Returns `true` if equals to string *s*, case-sensitive.

```
public static bool Eq(this ReadOnlySpan<char> t, ReadOnlySpan<char> s)
```

##### Parameters

- *t*  (`ReadOnlySpan<char>`):
    This span.
- *s*  (`ReadOnlySpan<char>`):
    Other string. Can be `null`.

##### Returns

`bool`

#### Remarks

Uses ordinal comparison (does not depend on current culture/locale).

* * *

## Overload 8

Compares part of this span with string *s*. Returns `true` if equal.

```
public static bool Eq(this ReadOnlySpan<char> t, int startIndex, ReadOnlySpan<char> s, bool ignoreCase = false)
```

##### Parameters

- *t*  (`ReadOnlySpan<char>`):
    This span.
- *startIndex*  (`int`):
    Offset in this span. If invalid, returns `false`.
- *s*  (`ReadOnlySpan<char>`):
    Other string.
- *ignoreCase*  (`bool`):
    Case-insensitive.

##### Returns

`bool`

##### Exceptions

- `ArgumentNullException`:
    *s* is `null`.

#### Remarks

Uses ordinal comparison (does not depend on current culture/locale).

* * *

## Overload 9

Returns `true` if the specified character is at the specified position in this span.

```
public static bool Eq(this ReadOnlySpan<char> t, int index, char c)
```

##### Parameters

- *t*  (`ReadOnlySpan<char>`):
    This span.
- *index*  (`int`):
    Offset in this span. If invalid, returns `false`.
- *c*  (`char`):
    Character.

##### Returns

`bool`