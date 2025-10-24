# Method `Au.More.Convert2.GzipDecompress`

## Overload 1

Decompresses data. Uses `System.IO.Compression.GZipStream`.

```
public static byte[] GzipDecompress(ReadOnlySpan<byte> compressed)
```

##### Parameters

- *compressed*  (`ReadOnlySpan<byte>`):
    Compressed data.

##### Returns

`byte[]`

Decompressed data.

##### Exceptions

- `Exception`:
    Exceptions of `System.IO.Compression.GZipStream`.

* * *

## Overload 2

Decompresses data to a caller-provided memory stream. Uses `System.IO.Compression.GZipStream`.

```
public static void GzipDecompress(ReadOnlySpan<byte> compressed, Stream decompressed)
```

##### Parameters

- *compressed*  (`ReadOnlySpan<byte>`):
    Compressed data.
- *decompressed*  (`Stream`):
    Stream for decompressed data.

##### Exceptions

- `Exception`:
    Exceptions of `System.IO.Compression.GZipStream`.