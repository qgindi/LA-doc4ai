# Method `Au.elm.Check`

## Overload 1

Checks or unchecks this checkbox or toggle-button, or selects this radio button. Uses `Au.elm.Invoke` or `Au.elm.SendKeys`.

```
public void Check(bool check = true, string keys = null)
```

##### Parameters

- *check*  (`bool`):
    `true` to check, `false` to uncheck.
- *keys*  (`string`):
    Keys for `Au.elm.SendKeys`. If `""`, uses `"Space"`. If `null` (default), uses `Au.elm.Invoke`.

##### Exceptions

- `Exception`:
    Exceptions of `Au.elm.Invoke` or `Au.elm.SendKeys`.

#### Remarks

Does nothing if the UI element already has the requested checked/unchecked state. Else tries to change the state and does not verify whether it actually worked.

Does not work with 3-state checkboxes and with elements that never have `CHECKED` state.

* * *

## Overload 2

Checks or unchecks this checkbox or toggle-button, or selects this radio button. To check/uncheck calls callback function.

```
public void Check(bool check, Action<elm> action)
```

##### Parameters

- *check*  (`bool`):
    `true` to check, `false` to uncheck.
- *action*  (`Action<Au.elm>`):
    Callback function that should check or uncheck this UI element. Its parameter is this variable.

##### Exceptions

- `Exception`:
    Exceptions of the callback function.

#### Remarks

Does nothing if the UI element already has the requested checked/unchecked state. Else tries to change the state and does not verify whether it actually worked.

Does not work with 3-state checkboxes and with elements that never have `CHECKED` state.