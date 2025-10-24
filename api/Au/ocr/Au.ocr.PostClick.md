# Method `Au.ocr.PostClick`

Posts mouse-click messages to the window, using coordinates in the found text (the first word).

```
public void PostClick(Coord x = default, Coord y = default, MButton button = MButton.Left, int word = 0)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X coordinate in the word. Default - center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate in the word. Default - center.
- *button*  (`Au.Types.MButton`):
    Can specify the left (default), right or middle button. Also flag for double-click, press or release.
- *word*  (`int`):
    Word index offset from `Au.ocr.FoundWordIndex`.

##### Exceptions

- `InvalidOperationException`:
    *area* is `Bitmap` or `screen`.
- `Au.Types.AuException`:
    Failed to get UI element rectangle (when searched in a UI element).

#### Remarks

Does not move the mouse. Does not wait until the target application finishes processing the message. Works not with all elements.