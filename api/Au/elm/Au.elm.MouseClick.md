# Method `Au.elm.MouseClick`

Clicks this UI element.

```
public MRelease MouseClick(Coord x = default, Coord y = default, MButton button = MButton.Left, int scroll = 0)
```

##### Parameters

- *x*  (`Au.Types.Coord`):
    X coordinate in the bounding rectangle of this UI element. Default - center. Examples: `10`, `^10` (reverse), `.5f` (fraction).
- *y*  (`Au.Types.Coord`):
    Y coordinate in the bounding rectangle of this UI element. Default - center.
- *button*  (`Au.Types.MButton`):
    Which button and how to use it.
- *scroll*  (`int`):
    If not 0, the function at first calls `Au.elm.ScrollTo`. If it succeeds, waits *scroll* number of milliseconds (let the target app update the UI element rectangle etc). Valid values are 0-5000. Tip: if does not scroll, try to find the UI element with flag `UIA`.

##### Returns

`Au.Types.MRelease`

##### Exceptions

- `Au.Types.AuException`:
    Failed to get UI element rectangle in container window (`Au.elm.WndContainer`).
- `Exception`:
    Exceptions of `Au.mouse.clickEx`.

#### Remarks

Calls `Au.mouse.clickEx`. To get rectangle in window, uses `Au.elm.GetRect` with *intersect* `true`.