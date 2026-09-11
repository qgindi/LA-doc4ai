# Class `Au.Types.OcrWord`

Stores text and rectangle of a word in OCR results.
See`Au.ocr.Words`.

```csharp
public record OcrWord : IEquatable<OcrWord>
```

##### Inheritance

`object` → `OcrWord`

### Constructors

`OcrWord(string, string, RECT, double)`

### Properties

`Offset`, `Rect`, `Separator`, `Text`