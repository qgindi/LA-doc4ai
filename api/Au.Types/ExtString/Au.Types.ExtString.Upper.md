# Method `Au.Types.ExtString.Upper`

## Overload 1

Converts this string to upper case.

```
public static string Upper(this string t)
```

##### Parameters

- *t*  (`string`):
    This string.

##### Returns

`string`

The result string.

#### Remarks

Calls `System.String.ToUpperInvariant`.

* * *

## Overload 2

Converts this string or only the first character to upper case or all words to title case.

```
public static string Upper(this string t, SUpper how, CultureInfo culture = null)
```

##### Parameters

- *t*  (`string`):
    This string.
- *how*  (`Au.Types.SUpper`)
- *culture*  (`CultureInfo`):
    Culture, for example `CultureInfo.CurrentCulture`. If `null` (default) uses invariant culture.

##### Returns

`string`

The result string.