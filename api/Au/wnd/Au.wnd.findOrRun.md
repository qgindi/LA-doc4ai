# Method `Au.wnd.findOrRun`

Finds a top-level window, like `Au.wnd.find`. If found, activates (optionally), else calls callback function and waits for the window. The callback should open the window, for example call `Au.run.it`.

```
public static wnd findOrRun(string name = null, string cn = null, WOwner of = default, WFlags flags = 0, Func<wnd, bool> also = null, WContains contains = default, Action run = null, Seconds? wait = null, bool activate = true)
```

##### Parameters

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
- *run*  (`Action`):
    Callback function. See example.
- *wait*  (`Au.Types.Seconds?`):
    How long to wait for the window after calling the callback function. Seconds. Default 60.
- *activate*  (`bool`):
    Activate the window. Default: `true`.

##### Returns

`Au.wnd`

Window handle as `Au.wnd`. On timeout returns `default(wnd)` if *wait* \< 0 (else exception).

##### Exceptions

- `Au.Types.NotFoundException`:
    *wait* time has expired (if >= 0).
- `Au.Types.AuWndException`:
    Failed to activate.
- `ArgumentException`:

    - *cn* is `""`. To match any, use `null`.
    - *of* is `""` or 0 or contains character `'\\'` or `'/'`. To match any, use `null`.
    - Invalid wildcard expression (`"**options "` or regular expression).

#### Examples

```
wnd w = wnd.findOrRun("* Notepad", run: () => run.it("notepad.exe"));
print.it(w);
```