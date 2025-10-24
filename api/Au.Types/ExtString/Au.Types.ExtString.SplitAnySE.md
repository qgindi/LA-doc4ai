# Method `Au.Types.ExtString.SplitAnySE`

## Overload 1

Splits this string into substrings as start/end offsets. Can be used multiple separators.

```
public static StartEnd[] SplitAnySE(this string t, Range range, ReadOnlySpan<char> separators, StringSplitOptions flags = StringSplitOptions.None)
```

##### Parameters

- *t*  (`string`)
- *range*  (`Range`)
- *separators*  (`ReadOnlySpan<char>`)
- *flags*  (`StringSplitOptions`)

##### Returns

`Au.Types.StartEnd[]`

* * *

## Overload 2

Splits this string into substrings as start/end offsets. Can be used multiple separators.

```
public static StartEnd[] SplitAnySE(this string t, Range range, ReadOnlySpan<string> separators, StringSplitOptions flags = StringSplitOptions.None)
```

##### Parameters

- *t*  (`string`)
- *range*  (`Range`)
- *separators*  (`ReadOnlySpan<string>`)
- *flags*  (`StringSplitOptions`)

##### Returns

`Au.Types.StartEnd[]`

* * *

## Overload 3

Splits this string span into substrings as start/end offsets. Can be used multiple separators.

```
public static StartEnd[] SplitAnySE(this ReadOnlySpan<char> t, ReadOnlySpan<char> separators, StringSplitOptions flags = StringSplitOptions.None)
```

##### Parameters

- *t*  (`ReadOnlySpan<char>`)
- *separators*  (`ReadOnlySpan<char>`)
- *flags*  (`StringSplitOptions`)

##### Returns

`Au.Types.StartEnd[]`

* * *

## Overload 4

Splits this string span into substrings as start/end offsets. Can be used multiple separators.

```
public static StartEnd[] SplitAnySE(this ReadOnlySpan<char> t, ReadOnlySpan<string> separators, StringSplitOptions flags = StringSplitOptions.None)
```

##### Parameters

- *t*  (`ReadOnlySpan<char>`)
- *separators*  (`ReadOnlySpan<string>`)
- *flags*  (`StringSplitOptions`)

##### Returns

`Au.Types.StartEnd[]`