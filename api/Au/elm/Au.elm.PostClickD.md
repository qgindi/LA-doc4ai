# Method `Au.elm.PostClickD`

Posts mouse-double-click messages to the container window, using coordinates in this UI element.

```
public void PostClickD(Coord x = default, Coord y = default)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X coordinate in the bounding rectangle of this UI element. Default - center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate in the bounding rectangle of this UI element. Default - center.

##### Exceptions

- `Au.Types.AuException`:

    - Failed to get rectangle or container window.
    - The element is invisible/offscreen.

#### Remarks

Does not move the mouse. Does not wait until the target application finishes processing the message. Works not with all elements. Try this function when `Au.elm.Invoke` does not work and you don't want to use `MouseClick`.