# Method `Au.Types.ExtString.LineCount`

## Overload 1

Returns the number of lines.

```
public static int LineCount(this string t, bool preferMore = false, Range? range = null, bool rareNewlines = false)
```

##### Parameters

- *t*  (`string`):
    This string.
- *preferMore*  (`bool`):
    Add 1 if the string ends with a line separator or its length is 0.
- *range*  (`Range?`):
    Part of this string or `null` (default).
- *rareNewlines*  (`bool`):
    If `false` (default), recognizes these newlines: `"\r\n"`, `"\n"` and `"\r"`. If `true`, also recognizes `"\f"`, `"\x0085"`, `"\x2028"` and `"\x2029"`.

##### Returns

`int`

##### Exceptions

- `ArgumentOutOfRangeException`

### See Also

`Au.More.StringUtil.LineAndColumn`

* * *

## Overload 2

Returns the number of lines.

```
public static int LineCount(this ReadOnlySpan<char> t, bool preferMore = false, bool rareNewlines = false)
```

##### Parameters

- *t*  (`ReadOnlySpan<char>`):
    This string.
- *preferMore*  (`bool`):
    Add 1 if the string ends with a line separator or its length is 0.
- *rareNewlines*  (`bool`):
    If `false` (default), recognizes these newlines: `"\r\n"`, `"\n"` and `"\r"`. If `true`, also recognizes `"\f"`, `"\x0085"`, `"\x2028"` and `"\x2029"`.

##### Returns

`int`

##### Exceptions

- `ArgumentOutOfRangeException`

### See Also

`Au.More.StringUtil.LineAndColumn`