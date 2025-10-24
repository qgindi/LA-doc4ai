# Class `Au.More.CaptureScreenImage`

Captures image pixels from screen or window.

```
public sealed class CaptureScreenImage : IDisposable
```

##### Remarks

This class is used by `Au.More.CaptureScreen`, `Au.uiimage` and `Au.uiimageFinder`. Also you can use it directly. For example it can get pixels directly without copying to a `System.Drawing.Bitmap` or array.

How to use:

1. Create variable.
2. Call `Au.More.CaptureScreenImage.Capture`.
3. Call other functions to get result in various formats.
4. If need, repeat 2-3 (for example when waiting for image).
5. Dispose (important).

Pixel format: `Format32bppArgb`, alpha 0xff.

##### Examples

```
var w = wnd.find("LibreAutomate").Child("document");

using var c = new CaptureScreenImage();
if (!c.Capture(w, new(0, 0, 200, 200))) return;
using var b = c.ToBitmap();

var f = folders.Temp + "test.png"; b.Save(f); run.it(f);
```

##### Inheritance

`object` → `CaptureScreenImage`

### Properties

`Height`, `Pixels`, `Width`

### Methods

`Capture`, `Capture`, `Dispose`, `ToArray1D`, `ToArray2D`, `ToBitmap`