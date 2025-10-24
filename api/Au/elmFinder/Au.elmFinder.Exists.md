# Method `Au.elmFinder.Exists`

## Overload 1

Finds the first matching descendant UI element in the window or UI element. Like `Au.elmFinder.Find`, just different return type.

```
public bool Exists()
```

##### Returns

`bool`

If found, sets `Au.elmFinder.Result` and returns `true`, else `false`.

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

* * *

## Overload 2

Finds the first matching descendant UI element in the window or UI element. Can wait and throw `Au.Types.NotFoundException`. Like `Au.elmFinder.Find`, just different return type.

```
public bool Exists(Seconds wait)
```

##### Parameters

- *wait*  (`Au.Types.Seconds`):
    The wait timeout, seconds. If 0, does not wait. If negative, does not throw exception when not found.

##### Returns

`bool`

If found, sets `Au.elmFinder.Result` and returns `true`. Else throws exception or returns `false` (if *wait* negative).

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