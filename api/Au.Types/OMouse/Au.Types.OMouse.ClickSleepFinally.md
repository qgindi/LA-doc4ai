# Property `Au.Types.OMouse.ClickSleepFinally`

How long to wait (milliseconds) before a "mouse click" or "mouse wheel" function returns. Default: 10.

```
public int ClickSleepFinally { get; set; }
```

##### Exceptions

- `ArgumentOutOfRangeException`

##### Property Value

`int`

Valid values: 0 - 10000 (10 s).

#### Remarks

The "click" functions also sleep `Au.Types.OMouse.ClickSpeed` ms after button down and up. Default `ClickSpeed` is 20, default `ClickSleepFinally` is 10, therefore default click time without mouse-move is 20+20+10=50.

#### Examples

```
opt.mouse.ClickSpeedFinally = 30;
```