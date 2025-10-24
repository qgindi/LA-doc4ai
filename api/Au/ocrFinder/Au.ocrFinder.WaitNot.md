# Method `Au.ocrFinder.WaitNot`

Performs OCR (text recognition) and waits until the specified text does not exist in results.

```
public bool WaitNot(Seconds timeout, IFArea area)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *area*  (`Au.Types.IFArea`):

    On-screen area or image:

    - `Au.wnd` - window or control (its client area).
    - `Au.elm` - UI element.
    - `System.Drawing.Bitmap` - image.
    - `Au.Types.RECT` - a rectangle area in screen.
    - `Au.Types.IFArea` - can contain `Au.wnd`, `Au.elm` or `System.Drawing.Bitmap`. Also allows to specify a rectangle in it, which makes the area smaller and the function faster. Example: `new(w, (left, top, width, height))`.

##### Returns

`bool`

Returns `true`. On timeout returns `false` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).
- `Au.Types.AuWndException`:
    Invalid window handle (the area argument), or the window closed while waiting.
- `ArgumentException`:
    An argument is/contains a `null`/invalid value.
- `Au.Types.AuException`:
    Something failed.

#### Remarks

The function captures image from screen or window (unless area is `System.Drawing.Bitmap`) and passes it to the OCR engine (calls `Au.Types.IOcrEngine.Recognize`). Then finds the specified text in results. If found, creates and returns an `Au.ocr` object that contains results.

The speed depends on engine, area size and amount of text.