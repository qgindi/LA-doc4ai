# Method `Au.Types.ExtString.Lines`

## Overload 1

Splits this string into lines.

```
public static string[] Lines(this string t, bool noEmpty = false, bool preferMore = false, bool rareNewlines = false)
```

##### Parameters

- *t*  (`string`):
    This string.
- *noEmpty*  (`bool`):
    Don't need empty lines.
- *preferMore*  (`bool`):
    Add 1 array element if the string ends with a line separator or its length is 0.
- *rareNewlines*  (`bool`):
    If `false` (default), recognizes these newlines: `"\r\n"`, `"\n"` and `"\r"`. If `true`, also recognizes `"\f"`, `"\x0085"`, `"\x2028"` and `"\x2029"`.

##### Returns

`string[]`

Array containing lines as strings. Does not include the last empty line, unless *preferMore* true.

### See Also

`System.IO.StringReader.ReadLine`

* * *

## Overload 2

Splits this string or a range in it into lines as start/end offsets.

```
public static StartEnd[] Lines(this string t, Range range, bool noEmpty = false, bool preferMore = false, bool rareNewlines = false)
```

##### Parameters

- *t*  (`string`):
    This string.
- *range*  (`Range`):
    Range of this string. Example: `var a = s.Lines(..); //split entire string`.
- *noEmpty*  (`bool`):
    Don't need empty lines.
- *preferMore*  (`bool`):
    Add 1 array element if the string range ends with a line separator or its length is 0.
- *rareNewlines*  (`bool`):
    If `false` (default), recognizes these newlines: `"\r\n"`, `"\n"` and `"\r"`. If `true`, also recognizes `"\f"`, `"\x0085"`, `"\x2028"` and `"\x2029"`.

##### Returns

`Au.Types.StartEnd[]`

Array containing start/end offsets of lines in the string (not in the range). Does not include the last empty line, unless *preferMore* true.

### See Also

`Au.Types.ExtString.Lines(ReadOnlySpan<char>, bool, bool, bool)`

* * *

## Overload 3

Splits this string into lines as start/end offsets.

```
public static StartEnd[] Lines(this ReadOnlySpan<char> t, bool noEmpty = false, bool preferMore = false, bool rareNewlines = false)
```

##### Parameters

- *t*  (`ReadOnlySpan<char>`):
    This string.
- *noEmpty*  (`bool`):
    Don't need empty lines.
- *preferMore*  (`bool`):
    Add 1 array element if the string span ends with a line separator or its length is 0.
- *rareNewlines*  (`bool`):
    If `false` (default), recognizes these newlines: `"\r\n"`, `"\n"` and `"\r"`. If `true`, also recognizes `"\f"`, `"\x0085"`, `"\x2028"` and `"\x2029"`.

##### Returns

`Au.Types.StartEnd[]`

Array containing start/end offsets of lines. Does not include the last empty line, unless *preferMore* true.