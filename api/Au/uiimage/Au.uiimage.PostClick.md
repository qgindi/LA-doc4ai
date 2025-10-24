# Method `Au.uiimage.PostClick`

Posts mouse-click messages to the window, using coordinates in the found image.

```
public void PostClick(Coord x = default, Coord y = default, MButton button = MButton.Left)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X coordinate in the found image. Default - center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate in the found image. Default - center.
- *button*  (`Au.Types.MButton`):
    Can specify the left (default), right or middle button. Also flag for double-click, press or release.

##### Exceptions

- `ArgumentException`:
    Unsupported button specified.
- `InvalidOperationException`:
    *area* is `Bitmap` or `screen`.
- `Au.Types.AuException`:
    Failed to get UI element rectangle (when searched in a UI element).

#### Remarks

Does not move the mouse. Does not wait until the target application finishes processing the message. Works not with all elements.