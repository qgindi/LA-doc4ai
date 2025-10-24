# Method `Au.More.Convert2.DeflateCompress`

Compresses data. Uses `System.IO.Compression.DeflateStream`.

```
public static byte[] DeflateCompress(ReadOnlySpan<byte> data)
```

##### Parameters

- *data*  (`ReadOnlySpan<byte>`):
    Data. See also: `System.Runtime.InteropServices.MemoryMarshal.AsBytes<T>`, `System.Runtime.InteropServices.CollectionsMarshal.AsSpan<T>`.

##### Returns

`byte[]`

##### Exceptions

- `Exception`:
    Exceptions of `System.IO.Compression.DeflateStream`.