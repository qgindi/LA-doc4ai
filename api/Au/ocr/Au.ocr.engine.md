# Property `Au.ocr.engine`

Gets or sets the default OCR engine.

```
public static IOcrEngine engine { get; set; }
```

##### Property Value

`Au.Types.IOcrEngine`

#### Remarks

If not set, the `get` function returns a static `Au.More.OcrWin10` object. To use another OCR engine, create and assign an object of type `Au.More.OcrWin10`, `Au.More.OcrTesseract`, `Au.More.OcrGoogleCloud`, `Au.More.OcrMicrosoftAzure` or other class that implements `Au.Types.IOcrEngine`.