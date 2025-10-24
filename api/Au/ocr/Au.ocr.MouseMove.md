# Method `Au.ocr.MouseMove`

Moves the mouse to the found text (the first word).

```
public void MouseMove(Coord x = default, Coord y = default, int word = 0)
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
    Exceptions of `Au.mouse.move`.

#### Remarks

Calls `Au.mouse.move`.