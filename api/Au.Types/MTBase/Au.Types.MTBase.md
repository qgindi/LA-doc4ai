# Class `Au.Types.MTBase`

Base class of `Au.popupMenu` and `Au.toolbar`.

```
public abstract class MTBase
```

##### Remarks

*image* argument of "add item" functions can be:

- icon name, like `"*Pack.Icon color"` (you can get it from the **Icons** tool). See `Au.More.ImageUtil.LoadWpfImageElement`.
- file/folder path (string) - the "show" function calls `Au.icon.of` to get its icon. It also supports file type icons like `".txt"`, etc.
- file path with prefix `"imagefile:"` or resource path that starts with `"resources/"` or has prefix `"resource:"` - the "show" function loads `.png` or `.xaml` image file or resource.
- string with prefix `"image:"` - Base64 encoded image file. Can be created with the **Find image** tool.
- `Au.Types.FolderPath` - same as folder path string.
- `System.Drawing.Image` - image.
- `Au.icon` - icon. The "add item" function disposes it.
- `Au.Types.StockIcon` - the "show" function calls `Au.icon.stock`.
- `null` - if `Au.Types.MTBase.ExtractIconPathFromCode` `true`, the "show" function tries to extract a file path from action code; then calls `Au.icon.of`. Else no image.
- string `""` - no image, even if `Au.Types.MTBase.ExtractIconPathFromCode` `true`.

Item images should be of size 16x16 (small icon size). If high DPI, will scale images automatically, which makes them slightly blurred. To avoid scaling, can be used XAML images, but then slower.

Images are loaded on demand, when showing the menu or submenu etc. If fails to load, prints warning (`Au.print.warning`).

For icon/image files use full path, unless they are in `Au.folders.ThisAppImages`

To add an image resource in Visual Studio, use build action **Resource** for the image file.

##### Inheritance

`object` → `MTBase`

Derived: `Au.popupMenu`, `Au.toolbar`

### Properties

`ActionException`, `ActionThread`, `ExtractIconPathFromCode`, `ImageSize`, `PathInTooltip`