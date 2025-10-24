# Method `Au.wnd.wait`

Waits until window exists or is active.

```
public static wnd wait(Seconds timeout, bool active, string name = null, string cn = null, WOwner of = default, WFlags flags = 0, Func<wnd, bool> also = null, WContains contains = default)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).
- *active*  (`bool`):
    The window must be the active window (`Au.wnd.active`), and not minimized.
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

##### Returns

`Au.wnd`

Window handle. On timeout returns `default(wnd)` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`:
    *timeout* time has expired (if > 0).
- `ArgumentException`

#### Remarks

Parameters etc are the same as `Au.wnd.find`. By default ignores invisible and cloaked windows. Use *flags* if need. If you have a window's `Au.wnd` variable, to wait until it is active/visible/etc use `Au.wnd.WaitFor<T>` instead.

#### Examples

```
wnd w = wnd.wait(10, false, "* Notepad");
print.it(w);
```

Using in a WPF window with async/await.

```
using System.Windows;
var b = new wpfBuilder("Window").WinSize(250);
b.R.AddButton("Wait", async _ => {
	  print.it("waiting for Notepad...");
	  wnd w = await Task.Run(() => wnd.wait(-10, false, "* Notepad"));
	  if(w.Is0) print.it("timeout"); else print.it(w);
});
if (!b.ShowDialog()) return;
```