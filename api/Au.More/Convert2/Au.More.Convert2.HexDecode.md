# Method `Au.More.Convert2.HexDecode`

## Overload 1

Converts hex-encoded string to binary data.

```
public static byte[] HexDecode(ReadOnlySpan<char> encoded)
```

##### Parameters

- *encoded*  (`ReadOnlySpan<char>`):
    String or `char[]` or span of string/array/memory containing hex encoded data.

##### Returns

`byte[]`

#### Remarks

Skips spaces and other non-hex-digit characters. Example: `"01 23 46 67"` is the same as `"01234667"`. The number of hex digit characters should be divisible by 2, else the last character is ignored.

* * *

## Overload 2

Converts hex-encoded string to binary data. Writes to caller's memory buffer.

```
public static int HexDecode(ReadOnlySpan<char> encoded, void* decoded, int bufferSize)
```

##### Parameters

- *encoded*  (`ReadOnlySpan<char>`):
    String or `char[]` or span of string/array/memory containing hex encoded data.
- *decoded*  (`void*`):
    Memory buffer for result.
- *bufferSize*  (`int`):
    Max number of bytes that can be written to the *decoded* memory buffer.

##### Returns

`int`

The number of bytes written in *decoded* memory. It is equal or less than `Math.Min(bufferSize, encoded.Length/2)`.

#### Remarks

Skips spaces and other non-hex-digit characters. Example: `"01 23 46 67"` is the same as `"01234667"`. The number of hex digit characters should be divisible by 2, else the last character is ignored.

* * *

## Overload 3

Converts hex-encoded string to a struct variable.

```
public static bool HexDecode<T>(ReadOnlySpan<char> encoded, out T decoded) where T : unmanaged
```

##### Parameters

- *encoded*  (`ReadOnlySpan<char>`):
    String or `char[]` or span of string/array/memory containing hex encoded data.
- *decoded*  (`T`):
    The result variable.

##### Returns

`bool`

`false` if decoded size != `sizeof(T)`.

##### Type Parameters

- `T`

#### Remarks

Skips spaces and other non-hex-digit characters. Example: `"01 23 46 67"` is the same as `"01234667"`. The number of hex digit characters should be divisible by 2, else the last character is ignored.