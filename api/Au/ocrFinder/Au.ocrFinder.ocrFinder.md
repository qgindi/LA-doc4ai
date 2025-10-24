# Constructor of `Au.ocrFinder`

Stores text to find and OCR parameters.

```
public ocrFinder(string text, OcrFlags flags = 0, double scale = 0, IOcrEngine engine = null, int skip = 0)
```

##### Parameters

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

##### Exceptions

- `ArgumentException`:
    *text* is empty or contains invalid regular expression.