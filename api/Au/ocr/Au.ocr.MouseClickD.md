# Method `Au.ocr.MouseClickD`

Double-clicks the found text (the first word).

```
public void MouseClickD(Coord x = default, Coord y = default, int word = 0)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X coordinate in the word. Default - center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate in the word. Default - center.
- *word*  (`int`):
    Word index offset from `Au.ocr.FoundWordIndex`.

##### Exceptions

- `InvalidOperationException`:
    *area* is `Bitmap`.
- `Exception`:
    Exceptions of `Au.mouse.clickEx`.

#### Remarks

Calls `Au.mouse.clickEx`.