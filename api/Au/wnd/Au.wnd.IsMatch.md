# Method `Au.wnd.IsMatch`

## Overload 1

Compares window name and other properties like `Au.wnd.find` does.

```
public bool IsMatch(string name = null, string cn = null, WOwner of = default, WFlags flags = 0, Func<wnd, bool> also = null, WContains contains = default)
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

`bool`

`true` if all specified (non-`null`/default) properties match.

##### Exceptions

- `ArgumentException`:

    - *cn* is `""`. To match any, use `null`.
    - *of* is `""` or 0 or contains character `'\\'` or `'/'`. To match any, use `null`.
    - Invalid wildcard expression (`"**options "` or regular expression).

#### Remarks

Creates new `Au.wndFinder` and calls `Au.wndFinder.IsMatch`. To compare single parameter, use more lightweight code. Examples: `if (w.Name.Like("* Notepad"))`, `if (w.ClassNameIs("CabinetWClass"))`.

### See Also

`Au.wnd.Name`

`Au.wnd.ClassName`

`Au.wnd.ClassNameIs`

`Au.wnd.ProgramName`

* * *

## Overload 2

Compares window name and other properties like `Au.wnd.find` does. Can be specified multiple windows.

```
public int IsMatch(ReadOnlySpan<wndFinder> windows)
```

##### Parameters

- *windows*  (`ReadOnlySpan<Au.wndFinder>`)

##### Returns

`int`

1-based index of the match, or 0 if none.

#### Examples

```
var w = wnd.active;
int i = w.IsMatch([new("name1", "class1"), new("name2", of: "program2")]);
print.it(i);
```

Cache finders to improve performance when IsMatch is called multiple times. Creating all finders each time is expensive.

```
class C {
	static wndFinder[] s_wf1;
	
	void F(wnd w) {
		int i = w.IsMatch(s_wf1 ??= [new("name1", "class1"), new("name2", of: "program2")]);
		print.it(i);
	}
}
```