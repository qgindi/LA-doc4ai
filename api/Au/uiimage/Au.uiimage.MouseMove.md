# Method `Au.uiimage.MouseMove`

Moves the mouse to the found image.

```
public void MouseMove(Coord x = default, Coord y = default)
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
    Exceptions of `Au.mouse.move`.

#### Remarks

Calls `Au.mouse.move`.