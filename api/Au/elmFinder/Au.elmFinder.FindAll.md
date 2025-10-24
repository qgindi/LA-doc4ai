# Method `Au.elmFinder.FindAll`

Finds all matching descendant UI elements in the window or UI element.

```
public elm[] FindAll()
```

##### Returns

`Au.elm[]`

Array of 0 or more elements.

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

See `Au.elmFinder.Find`.

#### Examples

```
var w = wnd.find(1, "", "Shell_TrayWnd");
print.it("---- buttons ----");
print.it(w.Elm["BUTTON"].FindAll());
print.it("---- all ----");
print.it(w.Elm.FindAll());
print.it("---- all buttons in elm at level 0 ----");
var e = w.Elm["TOOLBAR", "Running applications"].Find();
print.it(e.Elm["BUTTON", prop: "level=0"].FindAll());
print.it("---- all in elm ----");
print.it(e.Elm.FindAll());
```