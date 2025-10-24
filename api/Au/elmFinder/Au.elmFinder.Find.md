# Method `Au.elmFinder.Find`

## Overload 1

Finds the first matching descendant UI element in the window or UI element.

```
public elm Find()
```

##### Returns

`Au.elm`

If found, returns `Au.elmFinder.Result`, else `null`.

##### Exceptions

- `ArgumentException`:

    - *role* is `""` or invalid.
    - *name* is invalid wildcard expression (`"**options "` or regular expression).
    - *prop* contains unknown property names or errors in wildcard expressions.
    - *navig* string is invalid.
    - *flags* has `UIA` or `ClientArea` when searching in web page (role prefix `"web:"` etc) or `Au.elm`.
    - *role* has a prefix (`"web:"` etc) when searching in `Au.elm`.
    - `Au.elm.Item` not 0 when searching in `Au.elm`.
- `Au.Types.AuWndException`:
    Invalid window handle (0 or closed). See also `Au.elmFinder.In`.
- `Au.Types.AuException`:
    Failed. For example, window of a higher [UAC](../articles/UAC.html) integrity level process.

#### Remarks

To create code for this function, use tool **Find UI element**.

More info in `Au.elm` topic.

#### Examples

Find link `"Example"` in web page, and click. Wait max 5 s. Throw `Au.Types.NotFoundException` if not found.

```
var w = wnd.find(0, "* Chrome");
w.Elm["web:LINK", "Example"].Find(5).Invoke();
```

Try to find link `"Example"` in web page. Return if not found. Click if found.

```
var w = wnd.find(0, "* Chrome");
var e = w.Elm["web:LINK", "Example"].Find();
//var e = w.Elm["web:LINK", "Example"].Find(-5); //waits max 5 s
if(e == null) { print.it("not found"); return; }
e.Invoke();
```

* * *

## Overload 2

Finds the first matching descendant UI element in the window or UI element. Can wait and throw `Au.Types.NotFoundException`.

```
public elm Find(Seconds wait)
```

##### Parameters

- *wait*  (`Au.Types.Seconds`):
    The wait timeout, seconds. If 0, does not wait. If negative, does not throw exception when not found.

##### Returns

`Au.elm`

If found, returns `Au.elmFinder.Result`. Else throws exception or returns `null` (if *wait* negative).

##### Exceptions

- `Au.Types.NotFoundException`
- `ArgumentException`:

    - *role* is `""` or invalid.
    - *name* is invalid wildcard expression (`"**options "` or regular expression).
    - *prop* contains unknown property names or errors in wildcard expressions.
    - *navig* string is invalid.
    - *flags* has `UIA` or `ClientArea` when searching in web page (role prefix `"web:"` etc) or `Au.elm`.
    - *role* has a prefix (`"web:"` etc) when searching in `Au.elm`.
    - `Au.elm.Item` not 0 when searching in `Au.elm`.
- `Au.Types.AuWndException`:
    Invalid window handle (0 or closed). See also `Au.elmFinder.In`.
- `Au.Types.AuException`:
    Failed. For example, window of a higher [UAC](../articles/UAC.html) integrity level process.