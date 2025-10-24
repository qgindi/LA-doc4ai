# Method `Au.wnd.ButtonClick`

## Overload 1

Finds and clicks a button in this window. Does not use the mouse.

```
public void ButtonClick(int id)
```

##### Parameters

- *id*  (`int`):
    Control id of the button. See `Au.wnd.Child`.

##### Exceptions

- `Au.Types.AuWndException`:
    This variable is invalid (window not found, closed, etc).
- `Au.Types.NotFoundException`:
    Button not found.

#### Remarks

This function just calls `Au.wnd.Child` and `Au.mouse.postClick`. Uses this code: `mouse.postClick(this.Child(1, id: id));`

#### Examples

```
wnd.find("Options").ButtonClick(2);
```

* * *

## Overload 2

Finds and clicks a button in this window. Does not use the mouse.

```
public void ButtonClick(string name, bool asControl = false, string roleCN = null)
```

##### Parameters

- *name*  (`string`):
    Button name. String format: [wildcard expression](../articles/Wildcard%20expression.html).
- *asControl*  (`bool`):
    If `true`, finds/clicks as child control: `mouse.postClick(this.Child(1, name, roleCN ?? "*Button*"));`. If `false`, finds/clicks as UI element: `this.Elm[roleCN ?? "BUTTON", name].Find(1).Invoke();`. Default is `false`; it's slower but works with more windows.
- *roleCN*  (`string`):
    UI element role or control class name (if *asControl* `true`). String format: [wildcard expression](../articles/Wildcard%20expression.html). Default role is `"BUTTON"`, class name `"*Button*"`.

##### Exceptions

- `ArgumentException`:
    Invalid *name* (when starts with `"***"`). See `Au.elmFinder.this[]`, `Au.wnd.Child`.
- `Au.Types.AuWndException`:
    This variable is invalid (window not found, closed, etc).
- `Au.Types.NotFoundException`:
    Button not found.
- `Au.Types.AuException`:
    Failed to click. For example need to activate the window. No exception if *asControl* `true`.

#### Remarks

This function is just a shorter way to call other functions that have more options but require more code to call. If *asControl* `true`, it calls `Au.wnd.Child` and `Au.mouse.postClick`. Else `Au.wnd.Elm`, `Au.elmFinder.this[]`, `Au.elmFinder.Find` and `Au.elm.Invoke`.

#### Examples

```
wnd.find("Options").ButtonClick("Cancel");
```