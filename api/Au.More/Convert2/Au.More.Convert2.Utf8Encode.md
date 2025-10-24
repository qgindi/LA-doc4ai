# Method `Au.More.Convert2.Utf8Encode`

Converts string to UTF-8 `byte[]`. Can append `"\0"` (default) or some other string.

```
public static byte[] Utf8Encode(ReadOnlySpan<char> chars, string append = "\0")
```

##### Parameters

- *chars*  (`ReadOnlySpan<char>`):
    String or `char[]` or span of string/array/memory.
- *append*  (`string`):
    A string to append, or `null`. For example `"\0"` (default) or `"\r\n"`. Must contain only ASCII characters.

##### Returns

`byte[]`

##### Exceptions

- `ArgumentException`:
    *append* contains non-ASCII characters.