# Method `Au.elmFinder.Wait`

Waits for a matching descendant UI element to appear in the window or UI element.

```
public elm Wait(Seconds timeout)
```

##### Parameters

- *timeout*  (`Au.Types.Seconds`):
    Timeout, seconds. Can be 0 (infinite), >0 (exception) or \<0 (no exception). More info: [Wait timeout](../articles/Wait%20timeout.html).

##### Returns

`Au.elm`

If found, returns `Au.elmFinder.Result`. On timeout returns `null` if *timeout* is negative; else exception.

##### Exceptions

- `TimeoutException`
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

Same as `Au.elmFinder.Find`, except:

- 0 timeout means infinite.
- on timeout throws `System.TimeoutException`, not `Au.Types.NotFoundException`.