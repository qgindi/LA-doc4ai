# Method `Au.elm.PostClick`

Posts mouse-click messages to the container window, using coordinates in this UI element.

```
public void PostClick(Coord x = default, Coord y = default, MButton button = MButton.Left, int scroll = 0)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X coordinate in the bounding rectangle of this UI element. Default - center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate in the bounding rectangle of this UI element. Default - center.
- *button*  (`Au.Types.MButton`):
    Can specify the left (default), right or middle button. Also flag for double-click, press or release.
- *scroll*  (`int`):
    If not 0, the function calls `Au.elm.ScrollTo`. If it succeeds, waits *scroll* number of milliseconds (let the target app update the UI element rectangle etc). Valid values are 0-5000. Tip: if does not scroll, try to find the UI element with flag `UIA`.

##### Exceptions

- `Au.Types.AuException`:

    - Failed to get rectangle or container window.
    - The element is invisible/offscreen.
- `ArgumentException`:
    Unsupported button specified.

#### Remarks

Does not move the mouse. Does not wait until the target application finishes processing the message. Works not with all elements. Try this function when `Au.elm.Invoke` does not work and you don't want to use `MouseClick`.