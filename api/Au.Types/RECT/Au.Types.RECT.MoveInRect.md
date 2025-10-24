# Method `Au.Types.RECT.MoveInRect`

Moves this rectangle to the specified coordinates in another rectangle *r*.

```
public void MoveInRect(RECT r, Coord x = default, Coord y = default, bool ensureInRect = false)
```

##### Parameters

- *r*  (`Au.Types.RECT`):
    Another rectangle.
- *x*  (`Au.Types.Coord`):
    X coordinate relative to *r*. Default - center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate relative to *r*. Default - center.
- *ensureInRect*  (`bool`):
    If part of rectangle is not in *r*, move and/or resize it so that entire rectangle would be in *r*.