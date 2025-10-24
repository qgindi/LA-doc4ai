# Class `Au.More.OcrTesseract`

This OCR engine uses `tesseract.exe` from Tesseract installed on this computer.

```
public class OcrTesseract : IOcrEngine
```

##### Remarks

Slower than `Au.More.OcrWin10` (the default engine). The accuracy is poor. Supports more languages. You choose what languages to install when you install Tesseract.

[Download Tesseract](https://github.com/UB-Mannheim/tesseract/wiki)

##### Inheritance

`object` → `OcrTesseract`

### Constructors

`OcrTesseract(string)`

### Properties

`AvailableLanguages`, `CommandLine`, `DpiScale`, `Language`

### Methods

`Recognize`