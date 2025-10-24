# Method `Au.Types.IOcrEngine.PrepareBitmap`

If need, resizes the image and/or ensures it isn't too small.

```
protected static Bitmap PrepareBitmap(Bitmap b, bool dispose, double scale, int minWidth = 0, int minHeight = 0)
```

##### Parameters

- *b*  (`Bitmap`)
- *dispose*  (`bool`):
    Call `b.Dispose()` if created new image. The input image will not be used by the caller.
- *scale*  (`double`):
    Scale factor.
- *minWidth*  (`int`):
    Minimal image width accepted by the OCR engine.
- *minHeight*  (`int`):
    Minimal image height accepted by the OCR engine.

##### Returns

`Bitmap`