# Method `Au.mouse.wheel`

Mouse wheel forward or backward.

```
public static void wheel(double ticks, bool horizontal = false)
```

##### Parameters

- *ticks*  (`double`):
    Number of wheel ticks forward (positive) or backward (negative).
- *horizontal*  (`bool`):
    Horizontal wheel.

##### Exceptions

- `Au.Types.InputDesktopException`

#### Remarks

Uses `Au.opt.mouse`: `Au.Types.OMouse.ClickSleepFinally`.