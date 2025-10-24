# Property `Au.Types.OMouse.MoveSpeed`

If not 0, makes mouse movements slower, not instant. Default: 0.

```
public int MoveSpeed { get; set; }
```

##### Exceptions

- `ArgumentOutOfRangeException`

##### Property Value

`int`

Valid values: 0 (instant) - 10000 (slowest).

#### Remarks

Used by `Au.mouse.move`, `Au.mouse.click` and other functions that generate mouse movement events, except `Au.mouse.moveBy`. It is not milliseconds or some other unit. It adds intermediate mouse movements and small delays when moving the mouse cursor to the specified point. The speed also depends on the distance. Value 0 (default) does not add intermediate mouse movements. Adds at least 1 if some mouse buttons are pressed. Value 1 adds at least 1 intermediate mouse movement. Values 10-50 are good for visually slow movements.

#### Examples

```
opt.mouse.MoveSpeed = 30;
```