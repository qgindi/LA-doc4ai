# Method `Au.More.Convert2.BrotliCompress`

Compresses data. Uses `System.IO.Compression.BrotliEncoder`.

```
public static byte[] BrotliCompress(ReadOnlySpan<byte> data, int level = 6)
```

##### Parameters

- *data*  (`ReadOnlySpan<byte>`):
    Data. See also: `System.Runtime.InteropServices.MemoryMarshal.AsBytes<T>`, `System.Runtime.InteropServices.CollectionsMarshal.AsSpan<T>`.
- *level*  (`int`):
    Compression level, 0 (no compression) to 11 (maximal compression). Default 6. Bigger levels don't make much smaller but can make much slower.

##### Returns

`byte[]`

##### Exceptions

- `ArgumentOutOfRangeException`:
    Invalid *level*.
- `OutOfMemoryException`
- `Au.Types.AuException`:
    `System.IO.Compression.BrotliEncoder.TryCompress` failed.