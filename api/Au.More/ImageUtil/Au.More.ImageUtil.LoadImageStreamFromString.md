# Method `Au.More.ImageUtil.LoadImageStreamFromString`

Loads image file data as stream from Base64 string.

```
public static MemoryStream LoadImageStreamFromString(string s)
```

##### Parameters

- *s*  (`string`):
    Base64 encoded image string with prefix `"image:"`.

##### Returns

`MemoryStream`

##### Exceptions

- `ArgumentException`:
    String does not start with `"image:"` or is invalid Base64.
- `Exception`:
    `Au.More.Convert2.BrotliDecompress` exceptions (when compressed `.bmp`).