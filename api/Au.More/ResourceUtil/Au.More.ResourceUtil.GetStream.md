# Method `Au.More.ResourceUtil.GetStream`

Gets stream.

```
public static UnmanagedMemoryStream GetStream(string name)
```

##### Parameters

- *name*  (`string`):
    Resource name, like `"file.png"` or `"sub/file.png"`. More info: `Au.More.ResourceUtil`.

##### Returns

`UnmanagedMemoryStream`

##### Exceptions

- `FileNotFoundException`:
    Cannot find assembly or resource.
- `InvalidOperationException`:
    The resource type is not stream.
- `Exception`:
    Other exceptions that may be thrown by used .NET functions.

#### Remarks

Don't need to dispose the stream.