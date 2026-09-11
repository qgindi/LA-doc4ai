# Method `Au.Types.ExtString.SplitSE`

## Overload 1

Splits this string into substrings as start/end offsets.

```csharp
public static StartEnd[] SplitSE(this string t, Range range, char separator, StringSplitOptions flags = StringSplitOptions.None)
```

##### Parameters

- *t*  (`string`)
- *range*  (`Range`)
- *separator*  (`char`)
- *flags*  (`StringSplitOptions`):
  Enum: value__, None, RemoveEmptyEntries, TrimEntries, .ctor.

##### Returns

`Au.Types.StartEnd[]`

* * *

## Overload 2

Splits this string into substrings as start/end offsets.

```csharp
public static StartEnd[] SplitSE(this string t, Range range, string separator, StringSplitOptions flags = StringSplitOptions.None)
```

##### Parameters

- *t*  (`string`)
- *range*  (`Range`)
- *separator*  (`string`)
- *flags*  (`StringSplitOptions`):
  Enum: value__, None, RemoveEmptyEntries, TrimEntries, .ctor.

##### Returns

`Au.Types.StartEnd[]`

* * *

## Overload 3

Splits this string span into substrings as start/end offsets.

```csharp
public static StartEnd[] SplitSE(this ReadOnlySpan<char> t, char separator, StringSplitOptions flags = StringSplitOptions.None)
```

##### Parameters

- *t*  (`ReadOnlySpan<char>`)
- *separator*  (`char`)
- *flags*  (`StringSplitOptions`):
  Enum: value__, None, RemoveEmptyEntries, TrimEntries, .ctor.

##### Returns

`Au.Types.StartEnd[]`

* * *

## Overload 4

Splits this string span into substrings as start/end offsets.

```csharp
public static StartEnd[] SplitSE(this ReadOnlySpan<char> t, string separator, StringSplitOptions flags = StringSplitOptions.None)
```

##### Parameters

- *t*  (`ReadOnlySpan<char>`)
- *separator*  (`string`)
- *flags*  (`StringSplitOptions`):
  Enum: value__, None, RemoveEmptyEntries, TrimEntries, .ctor.

##### Returns

`Au.Types.StartEnd[]`