# Method `Au.More.Convert2.DeflateDecompress`

## Overload 1

Decompresses data. Uses `System.IO.Compression.DeflateStream`.

```
public static byte[] DeflateDecompress(ReadOnlySpan<byte> compressed)
```

##### Parameters

- *compressed*  (`ReadOnlySpan<byte>`):
    Compressed data.

##### Returns

`byte[]`

Decompressed data.

##### Exceptions

- `Exception`:
    Exceptions of `System.IO.Compression.DeflateStream`.

* * *

## Overload 2

Decompresses data to a caller-provided memory stream. Uses `System.IO.Compression.DeflateStream`.

```
public static void DeflateDecompress(ReadOnlySpan<byte> compressed, Stream decompressed)
```

##### Parameters

- *compressed*  (`ReadOnlySpan<byte>`):
    Compressed data.
- *decompressed*  (`Stream`):
    Stream for decompressed data.

##### Exceptions

- `Exception`:
    Exceptions of `System.IO.Compression.DeflateStream`.