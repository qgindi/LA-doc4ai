# Method `Au.More.ResourceUtil.GetGdipBitmap`

Gets GDI+ image.

```
public static Bitmap GetGdipBitmap(string name)
```

##### Parameters

- *name*  (`string`):
    Resource name, like `"file.png"` or `"sub/file.png"`. More info: `Au.More.ResourceUtil`.

##### Returns

`Bitmap`

##### Exceptions

- `FileNotFoundException`:
    Cannot find assembly or resource.
- `InvalidOperationException`:
    The resource type is not stream.
- `Exception`:
    Other exceptions that may be thrown by used .NET functions.