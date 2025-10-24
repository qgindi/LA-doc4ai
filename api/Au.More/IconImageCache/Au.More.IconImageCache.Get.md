# Method `Au.More.IconImageCache.Get`

Gets image from cache or file etc.

```
public Bitmap Get(string imageSource, int dpi, bool isImage, Action<string, Exception> onException = null)
```

##### Parameters

- *imageSource*  (`string`):
    File path, or resource path that starts with `"resources/"` or has prefix `"resource:"`, or icon name like `"*Pack.Icon color"`, etc. See *isImage* parameter.
- *dpi*  (`int`):
    DPI of window that will display the image. See `Au.More.Dpi`.
- *isImage*  (`bool`):

    `false` - get file/folder/filetype/url/etc icon with `Au.icon.of`. If *imageSource* is relative path of a `.cs` file, gets its custom icon as image; returns `null` if no custom icon or if editor isn't running. `true` - load image from xaml/png/etc file, database, resource or string with `Au.More.ImageUtil.LoadGdipBitmap` or `Au.More.ImageUtil.LoadWpfImageElement`. Can be icon name like `"*Pack.Icon color"` (see menu **Tools > Icons**).

    To detect whether a string is an image, call `Au.More.ImageUtil.HasImageOrResourcePrefix`; if it returns `true`, it is image.
- *onException*  (`Action<string, Exception>`):
    Action to call when fails to load image. If `null`, then silently returns `null`. Parameters are image source string and exception.

##### Returns

`Bitmap`