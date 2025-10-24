# Property `Au.Types.OMouse.MoveSleepFinally`

How long to wait (milliseconds) after moving the mouse cursor. Used in "move+click" functions too. Default: 10.

```
public int MoveSleepFinally { get; set; }
```

##### Exceptions

- `ArgumentOutOfRangeException`

##### Property Value

`int`

Valid values: 0 - 1000 (1 s).

#### Remarks

Used by `Au.mouse.move` (finally), `Au.mouse.click` (between moving and clicking) and other functions that generate mouse movement events.

#### Examples

```
opt.mouse.MoveSpeedFinally = 30;
```