# Method `Au.uiimageFinder.WaitNot`

See `Au.uiimage.waitNot`.

```
public bool WaitNot(Seconds timeout, IFArea area)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *area*  (`Au.Types.IFArea`):

    Where to search:

    - `Au.wnd` - window or control (its client area).
    - `Au.elm` - UI element.
    - `System.Drawing.Bitmap` - image.
    - `Au.Types.RECT` - a rectangle area in screen.
    - `Au.Types.IFArea` - can contain `Au.wnd`, `Au.elm` or `System.Drawing.Bitmap`. Also allows to specify a rectangle in it, which makes the area smaller and the function faster. Example: `new(w, (left, top, width, height))`.

##### Returns

`bool`

##### Exceptions

- `Exception`:
    Exceptions of `Au.uiimage.waitNot`, except those of the constructor.