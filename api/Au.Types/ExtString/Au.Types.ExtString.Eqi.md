# Method `Au.Types.ExtString.Eqi`

## Overload 1

Compares this and other string ignoring case (case-insensitive). Returns `true` if equal.

```
public static bool Eqi(this string t, string s)
```

##### Parameters

- *t*  (`string`):
    This string. Can be `null`.
- *s*  (`string`):
    Other string. Can be `null`.

##### Returns

`bool`

#### Remarks

Uses ordinal comparison (does not depend on current culture/locale).

* * *

## Overload 2

Returns `true` if equals to string *s*, case-insensitive.

```
public static bool Eqi(this ReadOnlySpan<char> t, ReadOnlySpan<char> s)
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