# Class `Au.More.OcrMicrosoftAzure`

This OCR engine uses Microsoft Azure Computer Vision OCR.

```
public class OcrMicrosoftAzure : IOcrEngine
```

##### Remarks

Sends image to Microsoft Azure and gets results. The OCR engine is accurate but much slower than the default engine or Tesseract, and usually slower than Google Cloud.

To use this engine, need to have a Microsoft Azure account and get API key and endpoint URL. The service isn't free, but 500 or so requests/month are free.

##### Inheritance

`object` → `OcrMicrosoftAzure`

### Constructors

`OcrMicrosoftAzure(string, string)`

### Properties

`DpiScale`

### Methods

`Recognize`