# Method `Au.uiimage.PostClickR`

Posts mouse-right-click messages to the window, using coordinates in the found image.

```
public void PostClickR(Coord x = default, Coord y = default)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X coordinate in the found image. Default - center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate in the found image. Default - center.

##### Exceptions

- `InvalidOperationException`:
    *area* is `Bitmap` or `screen`.
- `Au.Types.AuException`:
    Failed to get UI element rectangle (when searched in a UI element).

#### Remarks

Does not move the mouse. Does not wait until the target application finishes processing the message. Works not with all elements.