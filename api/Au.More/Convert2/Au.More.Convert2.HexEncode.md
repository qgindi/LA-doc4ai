# Method `Au.More.Convert2.HexEncode`

## Overload 1

Converts data in `byte[]` or other memory to hex-encoded string.

```
public static string HexEncode(ReadOnlySpan<byte> data, bool upperCase = false)
```

##### Parameters

- *data*  (`ReadOnlySpan<byte>`):
    Data. See also: `System.Runtime.InteropServices.MemoryMarshal.AsBytes<T>`, `System.Runtime.InteropServices.CollectionsMarshal.AsSpan<T>`.
- *upperCase*  (`bool`):
    Let the hex string contain A-F, not a-f.

##### Returns

`string`

#### Remarks

The result string length is 2 `*` data length. Often it's better to use `System.Convert.ToBase64String`, then result is 4/3 of data length. But cannot use Base64 in file names and URLs because it is case-sensitive and may contain character `'/'`. Both functions are fast.

* * *

## Overload 2

Converts binary data in any memory to hex-encoded string.

```
public static string HexEncode(void* data, int size, bool upperCase = false)
```

##### Parameters

- *data*  (`void*`):
    The data. Can be any valid memory of specified size, for example a struct address.
- *size*  (`int`):
    data memory size (bytes).
- *upperCase*  (`bool`):
    Let the hex string contain A-F, not a-f.

##### Returns

`string`

#### Remarks

The result string length is 2 `*` data length. Often it's better to use `System.Convert.ToBase64String`, then result is 4/3 of data length. But cannot use Base64 in file names and URLs because it is case-sensitive and may contain character `'/'`. Both functions are fast.

* * *

## Overload 3

Converts a struct variable to hex-encoded string.

```
public static string HexEncode<T>(T x, bool upperCase = false) where T : unmanaged
```

##### Parameters

- *x*  (`T`):
    Variable.
- *upperCase*  (`bool`):
    Let the hex string contain A-F, not a-f.

##### Returns

`string`

##### Type Parameters

- `T`

#### Remarks

The result string length is 2 `*` data length. Often it's better to use `System.Convert.ToBase64String`, then result is 4/3 of data length. But cannot use Base64 in file names and URLs because it is case-sensitive and may contain character `'/'`. Both functions are fast.