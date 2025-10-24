# Method `Au.ocr.MouseClick`

Clicks the found text (the first word).

```
public MRelease MouseClick(Coord x = default, Coord y = default, MButton button = MButton.Left, int word = 0)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X coordinate in the word. Default - center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate in the word. Default - center.
- *button*  (`Au.Types.MButton`):
    Which button and how to use it.
- *word*  (`int`):
    Word index offset from `Au.ocr.FoundWordIndex`.

##### Returns

`Au.Types.MRelease`

##### Exceptions

- `InvalidOperationException`:
    *area* is `Bitmap`.
- `Exception`:
    Exceptions of `Au.mouse.clickEx`.

#### Remarks

Calls `Au.mouse.clickEx`.