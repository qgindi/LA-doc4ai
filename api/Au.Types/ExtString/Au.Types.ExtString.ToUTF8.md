# Method `Au.Types.ExtString.ToUTF8`

## Overload 1

Converts to UTF-8 (`Encoding.UTF8.GetBytes`).

```
public static byte[] ToUTF8(this string t)
```

##### Parameters

- *t*  (`string`)

##### Returns

`byte[]`

* * *

## Overload 2

Converts to UTF-8.

```
public static byte[] ToUTF8(this ReadOnlySpan<char> t, bool append0 = false)
```

##### Parameters

- *t*  (`ReadOnlySpan<char>`)
- *append0*  (`bool`):
    Return 0-terminated UTF-8 string.

##### Returns

`byte[]`

* * *

## Overload 3

Converts to UTF-8.

```
public static byte[] ToUTF8(this Span<char> t, bool append0 = false)
```

##### Parameters

- *t*  (`Span<char>`)
- *append0*  (`bool`):
    Return 0-terminated UTF-8 string.

##### Returns

`byte[]`