# Method `Au.wnd.GetRectIn`

Gets rectangle of this window (usually control) relative to the client area of another window (usually parent).

```
public bool GetRectIn(wnd w, out RECT r)
```

##### Parameters

- *w*  (`Au.wnd`):
    Parent, ancestor or any other window or control. If `default(wnd)`, gets rectangle in screen.
- *r*  (`Au.Types.RECT`):
    Receives the rectangle.

##### Returns

`bool`

#### Remarks

Supports `Au.lastError`.

### See Also

`Au.wnd.RectInDirectParent`

`Au.wnd.RectInWindow`