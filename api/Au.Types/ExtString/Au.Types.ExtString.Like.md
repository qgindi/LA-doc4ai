# Method `Au.Types.ExtString.Like`

## Overload 1

Compares this string with a string that possibly contains wildcard characters. Returns `true` if the strings match.

```
public static bool Like(this string t, string pattern, bool ignoreCase = false)
```

##### Parameters

- *t*  (`string`):
    This string. If `null`, returns `false`. If `""`, returns `true` if *pattern* is `""` or `"*"`.
- *pattern*  (`string`):
    String that possibly contains wildcard characters. Cannot be `null`. If `""`, returns `true` if this string is `""`. If `"*"`, always returns `true` except when this string is `null`.
- *ignoreCase*  (`bool`):
    Case-insensitive.

##### Returns

`bool`

##### Exceptions

- `ArgumentNullException`:
    *pattern* is `null`.

#### Remarks

Wildcard characters:

| Character | Will match | Examples |
| --- | --- | --- |
| `*` | Zero or more of any characters. | `"start*"`, `"*end"`, `"*middle*"` |
| `?` | Any single character. | `"date ????-??-??"` |

There are no escape sequences for `*` and `?` characters.

Uses ordinal comparison, ie does not depend on current culture.

See also: [wildcard expression](../articles/Wildcard%20expression.html).

#### Examples

```
string s = @"C:\abc\mno.xyz";
if(s.Like(@"C:\abc\mno.xyz")) print.it("matches whole text (no wildcard characters)");
if(s.Like(@"C:\abc\*")) print.it("starts with");
if(s.Like(@"*.xyz")) print.it("ends with");
if(s.Like(@"*mno*")) print.it("contains");
if(s.Like(@"C:\*.xyz")) print.it("starts and ends with");
if(s.Like(@"?:*")) print.it("any character, : and possibly more text");
```

### See Also

`Au.wildex`

* * *

## Overload 2

Compares this string with a string that possibly contains wildcard characters. Returns `true` if the strings match.

```
public static bool Like(this ReadOnlySpan<char> t, string pattern, bool ignoreCase = false)
```

##### Parameters

- *t*  (`ReadOnlySpan<char>`):
    This string. If `null`, returns `false`. If `""`, returns `true` if *pattern* is `""` or `"*"`.
- *pattern*  (`string`):
    String that possibly contains wildcard characters. Cannot be `null`. If `""`, returns `true` if this string is `""`. If `"*"`, always returns `true` except when this string is `null`.
- *ignoreCase*  (`bool`):
    Case-insensitive.

##### Returns

`bool`

##### Exceptions

- `ArgumentNullException`:
    *pattern* is `null`.

* * *

## Overload 3

Calls `Au.Types.ExtString.Like(string, string, bool)` for each wildcard pattern specified in the argument list until it returns `true`. Returns 1-based index of the matching pattern, or 0 if none.

```
public static int Like(this string t, bool ignoreCase = false, params ReadOnlySpan<string> patterns)
```

##### Parameters

- *t*  (`string`)
- *ignoreCase*  (`bool`):
    Case-insensitive.
- *patterns*  (`ReadOnlySpan<string>`):
    One or more wildcard strings. The strings cannot be `null`.

##### Returns

`int`

##### Exceptions

- `ArgumentNullException`:
    A string in *patterns* is `null`.