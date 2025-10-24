# Method `Au.More.ResourceUtil.GetWpfImage`

Gets WPF image or icon that can be used as `ImageSource`.

```
public static BitmapFrame GetWpfImage(string name)
```

##### Parameters

- *name*  (`string`):
    Resource name, like `"file.png"` or `"sub/file.png"`. More info: `Au.More.ResourceUtil`.

##### Returns

`BitmapFrame`

##### Exceptions

- `FileNotFoundException`:
    Cannot find assembly or resource.
- `InvalidOperationException`:
    The resource type is not stream.
- `Exception`:
    Other exceptions that may be thrown by used .NET functions.