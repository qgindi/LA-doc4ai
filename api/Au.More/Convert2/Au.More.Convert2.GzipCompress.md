# Method `Au.More.Convert2.GzipCompress`

Compresses data. Uses `System.IO.Compression.GZipStream`.

```
public static byte[] GzipCompress(ReadOnlySpan<byte> data)
```

##### Parameters

- *data*  (`ReadOnlySpan<byte>`):
    Data. See also: `System.Runtime.InteropServices.MemoryMarshal.AsBytes<T>`, `System.Runtime.InteropServices.CollectionsMarshal.AsSpan<T>`.

##### Returns

`byte[]`

##### Exceptions

- `Exception`:
    Exceptions of `System.IO.Compression.GZipStream`.