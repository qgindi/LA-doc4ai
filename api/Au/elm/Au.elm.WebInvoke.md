# Method `Au.elm.WebInvoke`

Calls `Au.elm.Invoke` or *action* and waits until changes the web page (window name and page name).

```
public bool WebInvoke(Seconds? timeout = null, Action<elm> action = null)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds?`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html). Default 60 seconds.
- *action*  (`Action<Au.elm>`):
    If used, calls it instead of `Au.elm.Invoke`.

##### Returns

`bool`

Returns `true`. On timeout returns `false` if *timeout* \< 0; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).
- `Au.Types.AuException`:
    Failed. For example, when this UI element is invalid, or its top-level window does not contain a web page.
- `Au.Types.AuWndException`:
    The window was closed while waiting.
- `Exception`:
    Exceptions thrown by `Au.elm.Invoke` or by the *action* function.

#### Remarks

This function is used to click a link in a web page and wait until current web page is gone. It prevents a following "wait for UI element" function from finding a matching UI element in the old page, which would be bad. Does not wait until the new page is completely loaded. There is no reliable/universal way for it. Instead, after calling it you can call a "wait for UI element" function which waits for a known UI element that must be in the new page. This function cannot be used when the new page has the same title as current page. Then it waits until *timeout* time or forever. The same if the invoked action does not open a web page.