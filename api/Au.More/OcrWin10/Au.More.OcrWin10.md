# Class `Au.More.OcrWin10`

The default OCR engine. Available on Windows 10 and later.

```
public class OcrWin10 : IOcrEngine
```

##### Remarks

Uses the Windows 10/11 OCR engine. It's the fastest. The accuracy is poor. If need better accuracy, use a cloud OCR engine (`Au.More.OcrGoogleCloud`, `Au.More.OcrMicrosoftAzure`). If need a non-cloud OCR for older Windows, install Tesseract and use `Au.More.OcrTesseract`. Also it supports more languages.

##### Inheritance

`object` → `OcrWin10`

### Constructors

`OcrWin10()`

### Properties

`AvailableLanguages`, `DpiScale`, `Language`

### Methods

`Recognize`