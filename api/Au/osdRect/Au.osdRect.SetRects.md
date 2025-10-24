# Method `Au.osdRect.SetRects`

## Overload 1

Sets to draw multiple rectangles.

```
public void SetRects(IEnumerable<RECT> rects, bool indexLabels = false, ORLabelOptions labelOptions = null)
```

##### Parameters

- *rects*  (`IEnumerable<Au.Types.RECT>`):
    Rectangles.
- *indexLabels*  (`bool`):
    Draw labels. The label text is the rectangle index in *rects*.
- *labelOptions*  (`Au.Types.ORLabelOptions`):
    Label options. If `char` - label placement relative to rectangle: `'L'` (left), `'R'` (right), `'T'` (top), `'B'` (bottom) or `'I'` (inside). Default: `'L'`.

#### Remarks

If this function called, will draw multiple rectangles instead of single (unless *rects* is `null`). `Opacity` should be 0 (default).

* * *

## Overload 2

Sets to draw multiple rectangles with labels.

```
public void SetRects(IEnumerable<(RECT r, string s)> rects, ORLabelOptions labelOptions = null)
```

##### Parameters

- *rects*  (`IEnumerable<(RECT r, string s)>`):
    Rectangles with label text. The text should be short, single line, else may draw clipped.
- *labelOptions*  (`Au.Types.ORLabelOptions`):
    Label options. If `char` - label placement relative to rectangle: `'L'` (left), `'R'` (right), `'T'` (top), `'B'` (bottom) or `'I'` (inside). Default: `'L'`.

#### Remarks

If this function called, will draw multiple rectangles instead of single (unless *rects* is `null`). `Opacity` should be 0 (default).