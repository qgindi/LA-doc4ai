# Method `Au.Triggers.TriggerScopes.NotWindow`

## Overload 1

Sets scope "not this window". Hotkey, autotext and mouse triggers added afterwards will not work when the specified window is active.

```
public TriggerScope NotWindow(string name = null, string cn = null, WOwner of = default, Func<wnd, bool> also = null, WContains contains = default)
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
- *also*  (`Func<Au.wnd, bool>`):
    Callback function. Called for each matching window. It can evaluate more properties of the window and return `true` when they match. Example: `also: t => !t.IsPopupWindow`. Called after evaluating all other parameters except *contains*.
- *contains*  (`Au.Types.WContains`):

    Defines an object that must be in the client area of the window:

    - UI element: `Au.elmFinder` or string like `"name"` or `"e 'role' name"` or `"e 'role'"`.
    - Child control: `Au.wndChildFinder` or string like `"c 'cn' name"` or `"c '' name"` or `"c 'cn'"`.
    - Image(s) or color(s): `Au.uiimageFinder` or string `"image:..."` (uses a `Au.uiimageFinder` with flag `Au.Types.IFFlags.WindowDC`).
    - OCR text: `Au.ocrFinder` or string `"ocr:..."` (uses an `Au.ocrFinder` with flag `Au.Types.OcrFlags.WindowDC`).

##### Returns

`Au.Triggers.TriggerScope`

Returns an object that can be later passed to `Au.Triggers.TriggerScopes.Again` to reuse this scope.

##### Exceptions

- `ArgumentException`:

    - *cn* is `""`. To match any, use `null`.
    - *of* is `""` or 0 or contains character `'\\'` or `'/'`. To match any, use `null`.
    - Invalid wildcard expression (`"**options "` or regular expression).

#### Examples

`Au.Triggers.TriggerScopes`

* * *

## Overload 2

Sets scope "not this window". Hotkey, autotext and mouse triggers added afterwards will not work when the specified window is active.

```
public TriggerScope NotWindow(wndFinder f)
```

##### Parameters

- *f*  (`Au.wndFinder`)

##### Returns

`Au.Triggers.TriggerScope`

Returns an object that can be later passed to `Au.Triggers.TriggerScopes.Again` to reuse this scope.