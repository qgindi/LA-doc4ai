# Method `Au.More.ResourceUtil.GetXamlObject`

Gets WPF object from XAML resource, for example image.

```
public static object GetXamlObject(string name)
```

##### Parameters

- *name*  (`string`):
    Resource name, like `"file.xaml"` or `"sub/file.xaml"`. More info: `Au.More.ResourceUtil`.

##### Returns

`object`

An object of type of the XAML root object, for example `System.Windows.Controls.Viewbox` if `System.Windows.Controls.Image`.

##### Exceptions

- `FileNotFoundException`:
    Cannot find assembly or resource.
- `InvalidOperationException`:
    The resource type is not stream.
- `Exception`:
    Other exceptions that may be thrown by used .NET functions.