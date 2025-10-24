# Method `Au.uiimage.MouseClickR`

Right-clicks the found image.

```
public void MouseClickR(Coord x = default, Coord y = default)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X coordinate in the found image. Default - center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate in the found image. Default - center.

##### Exceptions

- `InvalidOperationException`:
    *area* is `Bitmap`.
- `Exception`:
    Exceptions of `Au.mouse.clickEx`.

#### Remarks

Calls `Au.mouse.clickEx`.