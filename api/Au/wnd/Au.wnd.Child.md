# Method `Au.wnd.Child`

## Overload 1

Finds a child control and returns its handle as `Au.wnd`.

```
public wnd Child(string name = null, string cn = null, WCFlags flags = 0, int? id = null, Func<wnd, bool> also = null, int skip = 0)
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
- *skip*  (`int`):
    0-based index of matching control. For example, if 1, the function skips the first matching control and returns the second.

##### Returns

`Au.wnd`

Returns `default(wnd)` if not found. See also: `Au.wnd.Is0`.

##### Exceptions

- `Au.Types.AuWndException`:
    This variable is invalid (window not found, closed, etc).
- `ArgumentException`:

    - *name* starts with `"***"`, but the prefix is invalid.
    - *cn* is `""`. To match any, use `null`.
    - Invalid wildcard expression (`"**options "` or regular expression).

#### Remarks

To create code for this function, use tool **Find window**.

* * *

## Overload 2

Finds a child control and returns its handle as `Au.wnd`. Can wait and throw `Au.Types.NotFoundException`.

```
public wnd Child(Seconds wait, string name = null, string cn = null, WCFlags flags = 0, int? id = null, Func<wnd, bool> also = null, int skip = 0)
```

##### Parameters

- *wait*  (`Au.Types.Seconds`):
    The wait timeout, seconds. If 0, does not wait. If negative, does not throw exception when not found.
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
- *skip*  (`int`):
    0-based index of matching control. For example, if 1, the function skips the first matching control and returns the second.

##### Returns

`Au.wnd`

Child control handle. If not found, throws exception or returns `default(wnd)` (if *wait* negative).

##### Exceptions

- `Au.Types.AuWndException`:
    This variable is invalid (window not found, closed, etc). Or closed while waiting.
- `Au.Types.NotFoundException`
- `ArgumentException`:

    - *name* starts with `"***"`, but the prefix is invalid.
    - *cn* is `""`. To match any, use `null`.
    - Invalid wildcard expression (`"**options "` or regular expression).

#### Remarks

To create code for this function, use tool **Find window**.