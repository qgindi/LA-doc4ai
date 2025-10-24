# Method `Au.wnd.waitAny`

Waits until any of specified windows exists or is active.

```
public static (int index, wnd w) waitAny(Seconds timeout, bool active, params wndFinder[] windows)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *active*  (`bool`):
    The window must be the active window (`Au.wnd.active`), and not minimized.
- *windows*  (`Au.wndFinder[]`):
    Specifies windows, like `new("Window1"), new("Window2")`.

##### Returns

`(int index, wnd w)`

1-based index and window handle. On timeout returns `(0, default(wnd))` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).

#### Remarks

By default ignores invisible and cloaked windows. Use `Au.wndFinder` flags if need.

#### Examples

```
var (i, w) = wnd.waitAny(10, true, new("* Notepad"), new("* Word"));
print.it(i, w);
```