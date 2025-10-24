# Method `Au.More.OcrTesseract.Recognize`

Recognizes text in image.

```
public OcrWord[] Recognize(Bitmap b, bool dispose, double scale)
```

##### Parameters

- *b*  (`Bitmap`):
    Image.
- *dispose*  (`bool`):
    Call `b.Dispose()`. The image will not be used by the caller.
- *scale*  (`double`):
    Scale factor.

##### Returns

`Au.Types.OcrWord[]`

Recognized words.

##### Implements

`Au.Types.IOcrEngine.Recognize(Bitmap, bool, double)`

#### Remarks

The class that implements this function can use static `Au.Types.IOcrEngine` functions to prepare the image (scale etc) and get image data.