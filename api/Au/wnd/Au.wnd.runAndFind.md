# Method `Au.wnd.runAndFind`

Opens and finds new window. Ignores old windows. Activates.

```
public static wnd runAndFind(Action run, Seconds timeout, string name = null, string cn = null, WOwner of = default, WFlags flags = 0, Func<wnd, bool> also = null, WContains contains = default, bool activate = true)
```

##### Parameters

- *run*  (`Action`):
    Callback function. Should open the window. See example.
- *timeout*  (`Au.Types.Seconds`):
    How long to wait for the window. Seconds. Can be 0 (infinite), >0 (exception on timeout) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *name*  (`string`):
    Window name. Usually it is the title bar text. String format: [wildcard expression](../articles/Wildcard%20expression.html). `null` means "can be any". `""` means "no name".
- *cn*  (`string`):
    Window class name. String format: [wildcard expression](../articles/Wildcard%20expression.html). `null` means "can be any". Cannot be `""`.
- *of*  (`Au.Types.WOwner`):

    Owner window, program or thread. Depends on argument type:

    - `Au.wnd` - owner window. Will use `Au.wnd.IsOwnedBy` with level 2.
    - `string` - program file name, like `"notepad.exe"`. String format: [wildcard expression](../articles/Wildcard%20expression.html). Cannot be `""` or path.
    - `Au.Types.WOwner` - `Au.Types.WOwner.Process`(process id), `Au.Types.WOwner.Thread`(thread id).

    See `Au.wnd.getwnd.Owner`, `Au.wnd.ProcessId`, `Au.process.thisProcessId`, `Au.wnd.ThreadId`, `Au.process.thisThreadId`.
- *flags*  (`Au.Types.WFlags`)
- *also*  (`Func<Au.wnd, bool>`):
    Callback function. Called for each matching window. It can evaluate more properties of the window and return `true` when they match. Example: `also: t => !t.IsPopupWindow`. Called after evaluating all other parameters except *contains*.
- *contains*  (`Au.Types.WContains`):

    Defines an object that must be in the client area of the window:

    - UI element: `Au.elmFinder` or string like `"name"` or `"e 'role' name"` or `"e 'role'"`.
    - Child control: `Au.wndChildFinder` or string like `"c 'cn' name"` or `"c '' name"` or `"c 'cn'"`.
    - Image(s) or color(s): `Au.uiimageFinder` or string `"image:..."` (uses a `Au.uiimageFinder` with flag `Au.Types.IFFlags.WindowDC`).
    - OCR text: `Au.ocrFinder` or string `"ocr:..."` (uses an `Au.ocrFinder` with flag `Au.Types.OcrFlags.WindowDC`).
- *activate*  (`bool`):
    Activate the window. Default: `true`.

##### Returns

`Au.wnd`

Window handle as `Au.wnd`. On timeout returns `default(wnd)` if *timeout* \< 0 (else exception).

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).
- `Au.Types.AuWndException`:
    Failed to activate.
- `ArgumentException`:

    - *cn* is `""`. To match any, use `null`.
    - *of* is `""` or 0 or contains character `'\\'` or `'/'`. To match any, use `null`.
    - Invalid wildcard expression (`"**options "` or regular expression).

#### Remarks

This function isn't the same as just two statements `Au.run.it` and `Au.wnd.find`. It never returns a window that already existed before calling it.

#### Examples

```
var w = wnd.runAndFind(
	() => run.it(folders.Windows + @"explorer.exe"),
	10, cn: "CabinetWClass");
print.it(w);
```