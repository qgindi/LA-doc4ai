# Constructor of `Au.Types.OcrWord`

```
public OcrWord(string separator, string text, RECT rect, double scale)
```

##### Parameters

- *separator*  (`string`):
    Separator before the word (space, new line, etc). Also can be `""` or `null`.
- *text*  (`string`):
    Word text.
- *rect*  (`Au.Types.RECT`):
    Word rectangle in *area*, possibly scaled.
- *scale*  (`double`):
    The *scale* parameter of the OCR function. This function unscales *rect* if need.