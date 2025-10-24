# Method `Au.More.ImageUtil.LoadWpfImage`

Loads WPF image or icon from file, resource or string.

```
public static BitmapFrame LoadWpfImage(string image)
```

##### Parameters

- *image*  (`string`):

    Can be:

    - file path. Can have prefix `"imagefile:"`.
    - resource path that starts with `"resources/"` or has prefix `"resource:"` (`Au.More.ResourceUtil.GetWpfImage`)
    - Base64 encoded image string with prefix `"image:"`.

##### Returns

`BitmapFrame`

##### Exceptions

- `Exception`