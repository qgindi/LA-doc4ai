# Constructor of `Au.More.BufferedPaint`

Gets non-buffered DC with API `BeginPaint` or `GetDC`. Then gets buffered DC with API `BeginBufferedPaint` for entire client area or rectangle *r*.

```
public BufferedPaint(wnd w, bool wmPaint, RECT? r = null)
```

##### Parameters

- *w*  (`Au.wnd`)
- *wmPaint*  (`bool`):
    Use API `BeginPaint`/`EndPaint`. If `false`, uses `GetDC`/`ReleaseDC`.
- *r*  (`Au.Types.RECT?`):
    Part of client area.