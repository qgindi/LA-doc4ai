# Indexer of `Au.Triggers.WindowTriggers`

## Overload 1

Adds a window trigger and its action.

```
public Action<WindowTriggerArgs> this[TWEvent winEvent, string name = null, string cn = null, WOwner of = default, Func<wnd, bool> also = null, WContains contains = default, TWFlags flags = 0, TWLater later = 0, string f_ = null, int l_ = 0] { set; }
```

##### Parameters

- *winEvent*  (`Au.Triggers.TWEvent`):
    Trigger event.
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
- *also*  (`Func<Au.wnd, bool>`):
    Callback function. Called for each matching window. It can evaluate more properties of the window and return `true` when they match. Example: `also: t => !t.IsPopupWindow`. Called after evaluating all other parameters except *contains*.
- *contains*  (`Au.Types.WContains`):

    Defines an object that must be in the client area of the window:

    - UI element: `Au.elmFinder` or string like `"name"` or `"e 'role' name"` or `"e 'role'"`.
    - Child control: `Au.wndChildFinder` or string like `"c 'cn' name"` or `"c '' name"` or `"c 'cn'"`.
    - Image(s) or color(s): `Au.uiimageFinder` or string `"image:..."` (uses a `Au.uiimageFinder` with flag `Au.Types.IFFlags.WindowDC`).
    - OCR text: `Au.ocrFinder` or string `"ocr:..."` (uses an `Au.ocrFinder` with flag `Au.Types.OcrFlags.WindowDC`).
- *flags*  (`Au.Triggers.TWFlags`):
    Trigger flags.
- *later*  (`Au.Triggers.TWLater`):
    Can optionally specify one or more additional events. This starts to work when the primary trigger is activated, and works only for that window. For example, to be notified when the window is closed or renamed, specify `later: TWLater.Destroyed | TWLater.Name`. When a "later" event occurs, the trigger action is executed. The `Au.Triggers.WindowTriggerArgs.Later` property then is that event; it is 0 when it is the primary trigger. The "later" triggers are not disabled when primary triggers are disabled.
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

##### Exceptions

- `InvalidOperationException`:
    Cannot add triggers after `Au.Triggers.ActionTriggers.Run` was called, until it returns.
- `ArgumentException`:
    See `Au.wnd.find`.

##### Property Value

`Action<Au.Triggers.WindowTriggerArgs>`

### See Also

`Au.Triggers.WindowTriggers.Last`

* * *

## Overload 2

Adds a window trigger and its action.

```
public Action<WindowTriggerArgs> this[TWEvent winEvent, wndFinder f, TWFlags flags = 0, TWLater later = 0, string f_ = null, int l_ = 0] { set; }
```

##### Parameters

- *winEvent*  (`Au.Triggers.TWEvent`):
    Trigger event.
- *f*  (`Au.wndFinder`)
- *flags*  (`Au.Triggers.TWFlags`):
    Trigger flags.
- *later*  (`Au.Triggers.TWLater`):
    Can optionally specify one or more additional events. This starts to work when the primary trigger is activated, and works only for that window. For example, to be notified when the window is closed or renamed, specify `later: TWLater.Destroyed | TWLater.Name`. When a "later" event occurs, the trigger action is executed. The `Au.Triggers.WindowTriggerArgs.Later` property then is that event; it is 0 when it is the primary trigger. The "later" triggers are not disabled when primary triggers are disabled.
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

##### Exceptions

- `InvalidOperationException`:
    Cannot add triggers after `Au.Triggers.ActionTriggers.Run` was called, until it returns.

##### Property Value

`Action<Au.Triggers.WindowTriggerArgs>`