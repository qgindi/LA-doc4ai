# Method `Au.uiimage.waitChanged`

Waits until something visually changes in a window or other area. More info: `Au.uiimage.find`.

```
public static bool waitChanged(Seconds timeout, IFArea area, IFFlags flags = 0, int diff = 0)
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
- *flags*  (`Au.Types.IFFlags`)
- *diff*  (`int`):
    Maximal allowed color difference. Can be 0 - 100, but should be as small as possible. Use to find images with slightly different colors than the specified image.

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

Like `Au.uiimage.waitNot`, but instead of *image* parameter this function captures the area image at the beginning.

#### Examples

Code created with tool **Find image or color in window**.

```
var w = wnd.find(1, "Window Name");
string image = "image:iVBORw0KGgoAAAANSUhEUgAAABYAAAANCAYAAACtpZ5jAAAAAXNSR0IArs4c...";
var im = uiimage.find(1, w, image);
im.MouseClick();
```