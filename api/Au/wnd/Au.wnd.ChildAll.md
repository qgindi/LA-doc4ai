# Method `Au.wnd.ChildAll`

Finds all matching child controls.

```
public wnd[] ChildAll(string name = null, string cn = null, WCFlags flags = 0, int? id = null, Func<wnd, bool> also = null)
```

##### Parameters

- *name*  (`string`):

    Control name. String format: [wildcard expression](../articles/Wildcard%20expression.html). `null` means "can be any". `""` means "no name".

    By default to get control names this function uses `Au.wnd.Name`. Can start with these prefix strings:

    - `"***text "` - use `Au.wnd.ControlText`. Slower and less reliable because can get editable text. If a character can be underlined with `Alt`, insert `'&'` before it.
    - `"***elmName "` - use `Au.wnd.NameElm`. Slower.
    - `"***wfName "` - use .NET Forms control name (see `Au.More.WinformsControlNames`). Slower and can fail because of [UAC](../articles/UAC.html).
- *cn*  (`string`):
    Control class name. String format: [wildcard expression](../articles/Wildcard%20expression.html). `null` means "can be any". Cannot be `""`.
- *flags*  (`Au.Types.WCFlags`)
- *id*  (`int?`):
    Control id. See `Au.wnd.ControlId`. Not used if `null` (default).
- *also*  (`Func<Au.wnd, bool>`):
    Callback function. Called for each matching control. It can evaluate more properties of the control and return `true` when they match. Example: `also: t => t.IsEnabled`

##### Returns

`Au.wnd[]`

Array containing zero or more `Au.wnd`.

##### Exceptions

- `Au.Types.AuWndException`:
    This variable is invalid (window not found, closed, etc).
- `ArgumentException`:

    - *name* starts with `"***"`, but the prefix is invalid.
    - *cn* is `""`. To match any, use `null`.
    - Invalid wildcard expression (`"**options "` or regular expression).

#### Remarks

Everything except the return type is the same as with `Au.wnd.Child`.

In the returned array, hidden controls (when using `Au.Types.WCFlags.HiddenToo`) are always after visible controls.

### See Also

`Au.wnd.getwnd.Children`