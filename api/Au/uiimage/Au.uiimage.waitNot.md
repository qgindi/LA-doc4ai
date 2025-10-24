# Method `Au.uiimage.waitNot`

Waits until image(s) or color(s) is not displayed in a window or other area. More info: `Au.uiimage.find`.

```
public static bool waitNot(Seconds timeout, IFArea area, IFImage image, IFFlags flags = 0, int diff = 0, Func<uiimage, IFAlso> also = null)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *area*  (`Au.Types.IFArea`):

    Where to search:

    - `Au.wnd` - window or control (its client area).
    - `Au.elm` - UI element.
    - `System.Drawing.Bitmap` - image.
    - `Au.Types.RECT` - a rectangle area in screen.
    - `Au.Types.IFArea` - can contain `Au.wnd`, `Au.elm` or `System.Drawing.Bitmap`. Also allows to specify a rectangle in it, which makes the area smaller and the function faster. Example: `new(w, (left, top, width, height))`.
- *image*  (`Au.Types.IFImage`):
    Image or color to find. Or array of them. More info: `Au.Types.IFImage`.
- *flags*  (`Au.Types.IFFlags`)
- *diff*  (`int`):
    Maximal allowed color difference. Can be 0 - 100, but should be as small as possible. Use to find images with slightly different colors than the specified image.
- *also*  (`Func<Au.uiimage, Au.Types.IFAlso>`):

    Callback function. Called for each found image instance and receives its rectangle, match index and list index. Can return one of `Au.Types.IFAlso` values. 
Examples:

    - Skip 2 matching images: `also: o => o.Skip(2)`
    - Skip some matching images if some condition is `false`: `also: o => condition ? IFAlso.OkReturn : IFAlso.FindOther`
    - Get rectangles etc of all matching images: `also: o => { list.Add(o); return IFAlso.OkFindMore; }`
    - Do different actions depending on which list images found: `var found = new BitArray(images.Length); uiimage.find(w, images, also: o => { found[o.ListIndex] = true; return IFAlso.OkFindMoreOfList; }); if(found[0]) print.it(0); if(found[1]) print.it(1);`

##### Returns

`bool`

Returns `true`. On timeout returns `false` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).
- `Au.Types.AuWndException`:
    Invalid window handle (the *area* argument), or the window closed while waiting.
- `ArgumentException`:
    An argument is/contains a `null`/invalid value.
- `FileNotFoundException`:
    Image file does not exist.
- `Exception`:
    Exceptions of `Au.More.ImageUtil.LoadGdipBitmap`.
- `Au.Types.AuException`:
    Something failed.

#### Remarks

To create code for this function, use tool **Find image or color in window**.

The speed mostly depends on:

1. The size of the search area. Use the smallest possible area (control or UI element or rectangle in window).
2. Flags `Au.Types.IFFlags.WindowDC` (makes faster), `Au.Types.IFFlags.PrintWindow`. The speed depends on window.
3. Video driver. Can be much slower if incorrect, generic or virtual PC driver is used. The above flags should help.
4. *diff*. Should be as small as possible.

If flag `Au.Types.IFFlags.WindowDC` or `Au.Types.IFFlags.PrintWindow` not used, the search area must be visible on the screen, because this function then gets pixels from the screen.

Can find only images that exactly match the specified image. With *diff* can find images with slightly different colors and brightness.

Transparent and partially transparent pixels of *image* are ignored. You can draw transparent areas with an image editor that supports it, for example Paint.NET.

This function is not the best way to find objects when the script is intended for long use or for use on multiple computers or must be very reliable. Because it may fail to find the image after changing some settings - system theme, application theme, text size (DPI), font smoothing (if the image contains text), etc. Also are possible various unexpected temporary conditions that may distort or hide the image, for example adjacent window shadow, a tooltip or some temporary window. If possible, in such scripts instead use other functions, eg find control or UI element.

Flags `Au.Types.IFFlags.WindowDC` and `Au.Types.IFFlags.PrintWindow` cannot be used if *area* is `Bitmap` or `Au.Types.RECT`.

#### Examples

Code created with tool **Find image or color in window**.

```
var w = wnd.find(1, "Window Name");
string image = "image:iVBORw0KGgoAAAANSUhEUgAAABYAAAANCAYAAACtpZ5jAAAAAXNSR0IArs4c...";
var im = uiimage.find(1, w, image);
im.MouseClick();
```