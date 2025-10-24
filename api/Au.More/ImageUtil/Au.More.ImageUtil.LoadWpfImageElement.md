# Method `Au.More.ImageUtil.LoadWpfImageElement`

Loads WPF image element from file, resource or string. Supports xaml, png and other image formats supported by WPF.

```
public static FrameworkElement LoadWpfImageElement(string image)
```

##### Parameters

- *image*  (`string`):

    Can be:

    - file path. Can be `.xaml`, `.png` etc. Supports environment variables etc, see `Au.pathname.expand`. Can have prefix `"imagefile:"`.
    - resource path that starts with `"resources/"` or has prefix `"resource:"`. This function calls `Au.More.ResourceUtil.GetXamlObject` if ends with `".xaml"`, else `Au.More.ResourceUtil.GetWpfImage`.
    - Base64 encoded image with prefix `"image:"`. See `Au.More.ImageUtil.LoadImageStreamFromString`.
    - XAML string that starts with `"<"`. For example from the **Icons** tool of LibreAutomate.
    - XAML icon name like `"*Pack.Icon color"` or `"*Pack.Icon color @size"` or `"*Pack1.Icon1 color1; *Pack2.Icon2 color2 %8,8,,"`. More info in Remarks.

##### Returns

`FrameworkElement`

If *image* is XAML icon name or starts with `"<"` or ends with `".xaml"` (case-insensitive), returns new WPF element of type specified by the XAML root element (uses `System.Windows.Markup.XamlReader`). Else returns `System.Windows.Controls.Image` with `Source` = `System.Windows.Media.Imaging.BitmapFrame` (uses `Au.More.ImageUtil.LoadWpfImage`).

##### Exceptions

- `Exception`

#### Remarks

*image* can be an XAML icon name from the **Icons** tool of LibreAutomate (LA), like `"*Pack.Icon color"`. Full format: `"[*<library>]*pack.name[ color][ @size][ %margin][;more icons]"`. Here parts enclosed in `[]` are optional. The color, size and margin parts can be in any order.

- color - `#RRGGBB` or color name (WPF). If 2 colors like `"#008000|#00FF00"`, the second color is for high contrast dark theme. If omitted, will use the system color of control text. Also can be like `"#008000|"` to use control text only for dark contrast theme, or `"|#00FF00"` for vice versa.
- size - icon size 1 to 16, like `"*Pack.Icon blue @12"`. Can be used to make the displayed icon smaller or in some cases less blurry. It is the logical width and height of the icon rendered at the center of a box of logical size 16x16. To make icon bigger, instead set properties `Width` and `Height` of the returned element; or `Au.Types.MTBase.ImageSize` for a toolbar or menu.
- margin - icon margins inside a box of logical size 16x16. Format: `%left,top,right,bottom,stretch,snap`. All parts are optional. Examples: `"*Pack.Icon blue %,,8,8"`, `"*Pack.Icon blue %8,8"`, `"*Pack.Icon blue %4,,4,,f"`. The stretch part can be `f` (fill) or `m` (move); default is uniform. The snap part can be `p` (sets `SnapsToDevicePixels=True`). Can be used either margin or size, not both.
- more icons - can be specified multiple icons separated by semicolon, like `"*Pack1.Icon1 color1; *Pack2.Icon2 color2"`. It allows to create multi-color icons (for example a "filled" icon of one color + an "outline" icon of another color) or to add a small overlay icon (eg to indicate disabled state) at a corner (use margin).
- library - name of assembly containing the resource. If omitted, uses `System.Reflection.Assembly.GetEntryAssembly`. 
The LA compiler finds icon strings anywhere in code, gets their XAML from the database, and adds the XAML to the assembly as a string resource (see **Properties > Resource > Options**). This function gets the XAML from resources (`Au.More.ResourceUtil.GetString`). If fails, then tries to get XAML from database, and fails if LA isn't running. Uses `Au.More.ScriptEditor.GetIcon`.