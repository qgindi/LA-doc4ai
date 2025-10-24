# Method `Au.ocr.find`

## Overload 1

Performs OCR (text recognition) and finds text in results.

```
public static ocr find(IFArea area, string text, OcrFlags flags = 0, double scale = 0, IOcrEngine engine = null, int skip = 0)
```

##### Parameters

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

`Au.ocr`

Returns an `Au.ocr` object that contains the word index and can click it etc. Returns `null` if not found.

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

* * *

## Overload 2

Performs OCR (text recognition) and finds text in results. Can wait and throw `Au.Types.NotFoundException`.

```
public static ocr find(Seconds wait, IFArea area, string text, OcrFlags flags = 0, double scale = 0, IOcrEngine engine = null, int skip = 0)
```

##### Parameters

- *wait*  (`Au.Types.Seconds`):
    The wait timeout, seconds. If 0, does not wait. If negative, does not throw exception when not found.
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

`Au.ocr`

Returns an `Au.ocr` object that contains the word index and can click it etc. If not found, throws exception or returns `null` (if *wait* negative).

##### Exceptions

- `Au.Types.NotFoundException`
- `Au.Types.AuWndException`:
    Invalid window handle (the area argument), or the window closed while waiting.
- `ArgumentException`:
    An argument is/contains a `null`/invalid value.
- `Au.Types.AuException`:
    Something failed.

#### Remarks

The function captures image from screen or window (unless area is `System.Drawing.Bitmap`) and passes it to the OCR engine (calls `Au.Types.IOcrEngine.Recognize`). Then finds the specified text in results. If found, creates and returns an `Au.ocr` object that contains results.

The speed depends on engine, area size and amount of text.