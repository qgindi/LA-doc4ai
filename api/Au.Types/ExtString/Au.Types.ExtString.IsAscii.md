# Method `Au.Types.ExtString.IsAscii`

## Overload 1

Returns `true` if does not contain non-ASCII characters.

```
public static bool IsAscii(this string t)
```

##### Parameters

- *t*  (`string`)

##### Returns

`bool`

* * *

## Overload 2

Returns `true` if does not contain non-ASCII characters.

```
public static bool IsAscii(this ReadOnlySpan<char> t)
```

##### Parameters

- *t*  (`ReadOnlySpan<char>`)

##### Returns

`bool`

* * *

## Overload 3

Returns `true` if does not contain non-ASCII character bytes.

```
public static bool IsAscii(this ReadOnlySpan<byte> t)
```

##### Parameters

- *t*  (`ReadOnlySpan<byte>`)

##### Returns

`bool`