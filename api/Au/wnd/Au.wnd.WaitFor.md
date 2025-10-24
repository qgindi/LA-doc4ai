# Method `Au.wnd.WaitFor`

Waits for a user-defined state/condition of this window. For example active, visible, enabled, closed, contains something.

```
public T WaitFor<T>(Seconds timeout, Func<wnd, T> condition, bool dontThrowIfClosed = false)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *condition*  (`Func<Au.wnd, T>`):
    Callback function (eg lambda). It is called repeatedly, until returns a value other than `default(T)`, for example `true`.
- *dontThrowIfClosed*  (`bool`):
    Do not throw exception when the window handle is invalid or the window was closed while waiting. In such case the callback function must return a non-default value, like in examples with `Au.wnd.IsAlive`. Else exception is thrown (with a small delay) to prevent infinite waiting.

##### Returns

`T`

Returns the value returned by the callback function. On timeout returns `default(T)` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).
- `Au.Types.AuWndException`:
    The window handle is invalid or the window was closed while waiting.

##### Type Parameters

- `T`

#### Examples

```
wnd w = wnd.find("* Notepad");

//wait max 30 s until window w is active. Exception on timeout or if closed.
w.WaitFor(30, t => t.IsActive);
print.it("active");

//wait max 30 s until window w is enabled. Exception on timeout or if closed.
w.WaitFor(30, t => t.IsEnabled);
print.it("enabled");

//wait until window w is closed
w.WaitFor(0, t => !t.IsAlive, true); //same as w.WaitForClosed()
print.it("closed");

//wait until window w is minimized or closed
w.WaitFor(0, t => t.IsMinimized || !t.IsAlive, true);
if(!w.IsAlive) { print.it("closed"); return; }
print.it("minimized");

//wait until window w contains focused control classnamed "Edit"
var c = new wndChildFinder(cn: "Edit");
w.WaitFor(10, t => c.Exists(t) && c.Result.IsFocused);
print.it("control focused");
```