# Method `Au.elm.MouseMove`

Moves the cursor (mouse pointer) to this UI element.

```
public void MouseMove(Coord x = default, Coord y = default, int scroll = 0)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X coordinate in the bounding rectangle of this UI element. Default - center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate in the bounding rectangle of this UI element. Default - center.
- *scroll*  (`int`):
    If not 0, the function at first calls `Au.elm.ScrollTo`. If it succeeds, waits *scroll* number of milliseconds (let the target app update the UI element rectangle etc).

##### Exceptions

- `Au.Types.AuException`:
    Failed to get UI element rectangle in container window (`Au.elm.WndContainer`).
- `Exception`:
    Exceptions of `Au.mouse.move`.

#### Remarks

Calls `Au.mouse.move`. To get rectangle in window, uses `Au.elm.GetRect` with *intersect* `true`.