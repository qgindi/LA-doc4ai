# Method `Au.ocr.waitNot`

Performs OCR (text recognition) and waits until the specified text does not exist in results.

```
public static bool waitNot(Seconds timeout, IFArea area, string text, OcrFlags flags = 0, double scale = 0, IOcrEngine engine = null, int skip = 0)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *area*  (`Au.Types.IFArea`):

    On-screen area or image:

    - `Au.wnd` - window or control (its client area).
    - `Au.elm` - UI element.
    - `System.Drawing.Bitmap` - image.
    - `Au.Types.RECT` - a rectangle area in screen.
    - `Au.Types.IFArea` - can contain `Au.wnd`, `Au.elm` or `System.Drawing.Bitmap`. Also allows to specify a rectangle in it, which makes the area smaller and the function faster. Example: `new(w, (left, top, width, height))`.
- *text*  (`string`):

    Text to find in `Au.ocr.TextForFind`. Can have prefix:

    - `"**r "` - PCRE regular expression. Example: `@"**r \bwhole words\b"`.
    - `"**R "` - .NET regular expression.
    - `"**i "` - case-insensitive.
    - `"**t "` - case-sensitive (default).
- *flags*  (`Au.Types.OcrFlags`)
- *scale*  (`double`):
    Scale factor (how much to resize the image before performing OCR). Value 2 or 3 may improve results of OCR engine `Au.More.OcrWin10` or `Au.More.OcrTesseract`. If 0 (default), depends on engine's `Au.Types.IOcrEngine.DpiScale` and area's DPI.
- *engine*  (`Au.Types.IOcrEngine`):
    OCR engine. Default: `Au.ocr.engine` (`Au.More.OcrWin10` if not specified).
- *skip*  (`int`):
    Skip this count of found text instances.

##### Returns

`bool`

Returns `true`. On timeout returns `false` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).
- `Au.Types.AuWndException`:
    Invalid window handle (the area argument), or the window closed while waiting.
- `ArgumentException`:
    An argument is/contains a `null`/invalid value.
- `Au.Types.AuException`:
    Something failed.

#### Remarks

The function captures image from screen or window (unless area is `System.Drawing.Bitmap`) and passes it to the OCR engine (calls `Au.Types.IOcrEngine.Recognize`). Then finds the specified text in results. If found, creates and returns an `Au.ocr` object that contains results.

The speed depends on engine, area size and amount of text.