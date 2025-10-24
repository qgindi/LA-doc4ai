# Method `Au.wnd.find`

## Overload 1

Finds a top-level window and returns its handle as `Au.wnd`.

```
public static wnd find(string name = null, string cn = null, WOwner of = default, WFlags flags = 0, Func<wnd, bool> also = null, WContains contains = default)
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

##### Returns

`Au.wnd`

Window handle, or `default(wnd)` if not found. See also: `Au.wnd.Is0`.

##### Exceptions

- `ArgumentException`:

    - *cn* is `""`. To match any, use `null`.
    - *of* is `""` or 0 or contains character `'\\'` or `'/'`. To match any, use `null`.
    - Invalid wildcard expression (`"**options "` or regular expression).

#### Remarks

To create code for this function, use tool **Find window**.

If there are multiple matching windows, gets the first in the Z order matching window, preferring visible windows.

On Windows 8 and later may skip Windows Store app Metro-style windows (on Windows 10 few such windows exist). It happens if this program does not have `disableWindowFiltering = true` in its manifest and is not uiAccess; to find such windows you can use `Au.wnd.findFast`.

To find message-only windows use `Au.wnd.findFast` instead.

#### Examples

Try to find Notepad window. Return if not found.

```
wnd w = wnd.find("* Notepad");
if(w.Is0) { print.it("not found"); return; }
```

Try to find Notepad window. Throw `Au.Types.NotFoundException` if not found.

```
wnd w1 = wnd.find(0, "* Notepad");
```

Wait for Notepad window max 3 seconds. Throw `Au.Types.NotFoundException` if not found during that time.

```
wnd w1 = wnd.find(3, "* Notepad");
```

Wait for Notepad window max 3 seconds. Return if not found during that time.

```
wnd w1 = wnd.find(-3, "* Notepad");
if(w.Is0) { print.it("not found"); return; }
```

Wait for Notepad window max 3 seconds. Throw `Au.Types.NotFoundException` if not found during that time. When found, wait max 1 s until becomes active, then activate.

```
wnd w1 = wnd.find(3, "* Notepad").Activate(1);
```

* * *

## Overload 2

Finds a top-level window and returns its handle as `Au.wnd`. Can wait and throw `Au.Types.NotFoundException`.

```
public static wnd find(Seconds wait, string name = null, string cn = null, WOwner of = default, WFlags flags = 0, Func<wnd, bool> also = null, WContains contains = default)
```

##### Parameters

- *wait*  (`Au.Types.Seconds`):
    The wait timeout, seconds. If 0, does not wait. If negative, does not throw exception when not found.
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

Window handle. If not found, throws exception or returns `default(wnd)` (if *wait* negative).

##### Exceptions

- `Au.Types.NotFoundException`
- `ArgumentException`:

    - *cn* is `""`. To match any, use `null`.
    - *of* is `""` or 0 or contains character `'\\'` or `'/'`. To match any, use `null`.
    - Invalid wildcard expression (`"**options "` or regular expression).