# Method `Au.uiimage.MouseClick`

Clicks the found image.

```
public MRelease MouseClick(Coord x = default, Coord y = default, MButton button = MButton.Left)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X coordinate in the found image. Default - center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate in the found image. Default - center.
- *button*  (`Au.Types.MButton`):
    Which button and how to use it.

##### Returns

`Au.Types.MRelease`

##### Exceptions

- `InvalidOperationException`:
    *area* is `Bitmap`.
- `Exception`:
    Exceptions of `Au.mouse.clickEx`.

#### Remarks

Calls `Au.mouse.clickEx`.