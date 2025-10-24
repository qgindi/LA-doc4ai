# Method `Au.More.Convert2.BrotliDecompress`

Decompresses data. Uses `System.IO.Compression.BrotliDecoder`.

```
public static byte[] BrotliDecompress(ReadOnlySpan<byte> compressed)
```

##### Parameters

- *compressed*  (`ReadOnlySpan<byte>`):
    Compressed data.

##### Returns

`byte[]`

Decompressed data.

##### Exceptions

- `ArgumentException`:
    Invalid data.
- `OutOfMemoryException`