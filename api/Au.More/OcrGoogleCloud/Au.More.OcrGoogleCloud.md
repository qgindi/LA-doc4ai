# Class `Au.More.OcrGoogleCloud`

This OCR engine uses [Google Cloud Vision API](https://cloud.google.com/vision/docs/reference/rest/v1/images/annotate).

```
public class OcrGoogleCloud : IOcrEngine
```

##### Remarks

Sends image to Google Cloud and gets results. The OCR engine is accurate but much slower than the default engine or Tesseract. Depends on internet connection speed.

To use this engine, need to have a Google Cloud account, enable Vision API and get API key. The service isn't free, but 1000 or so requests/month are free.

##### Inheritance

`object` → `OcrGoogleCloud`

### Constructors

`OcrGoogleCloud(string)`

### Properties

`DpiScale`, `Features`, `ImageContext`

### Methods

`Recognize`