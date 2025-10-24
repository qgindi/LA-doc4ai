# Method `Au.ocr.recognize`

Performs OCR (text recognition).

```
public static ocr recognize(IFArea area, OcrFlags flags = 0, double scale = 0, IOcrEngine engine = null)
```

##### Parameters

- *area*  (`Au.Types.IFArea`):

    On-screen area or image:

    - `Au.wnd` - window or control (its client area).
    - `Au.elm` - UI element.
    - `System.Drawing.Bitmap` - image.
    - `Au.Types.RECT` - a rectangle area in screen.
    - `Au.Types.IFArea` - can contain `Au.wnd`, `Au.elm` or `System.Drawing.Bitmap`. Also allows to specify a rectangle in it, which makes the area smaller and the function faster. Example: `new(w, (left, top, width, height))`.
- *flags*  (`Au.Types.OcrFlags`)
- *scale*  (`double`):
    Scale factor (how much to resize the image before performing OCR). Value 2 or 3 may improve results of OCR engine `Au.More.OcrWin10` or `Au.More.OcrTesseract`. If 0 (default), depends on engine's `Au.Types.IOcrEngine.DpiScale` and area's DPI.
- *engine*  (`Au.Types.IOcrEngine`):
    OCR engine. Default: `Au.ocr.engine` (`Au.More.OcrWin10` if not specified).

##### Returns

`Au.ocr`

Returns an `Au.ocr` object that contains recognized words etc. Returns `null` if the area is empty.

##### Exceptions

- `Au.Types.AuWndException`:
    Invalid window handle (the *area* argument).
- `ArgumentException`:
    An argument is/contains a `null`/invalid value.
- `Au.Types.AuException`:
    Something failed.

#### Remarks

The function captures image from screen or window (unless area is `System.Drawing.Bitmap`) and passes it to the OCR engine (calls `Au.Types.IOcrEngine.Recognize`). Then finds the specified text in results. If found, creates and returns an `Au.ocr` object that contains results.

The speed depends on engine, area size and amount of text.